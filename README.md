# Portal de Tutoriais e Laboratórios (Engenharia/UFSC)

Bem-vindo ao portal de documentação e tutoriais práticos. Este espaço foi desenvolvido para centralizar os roteiros de aprendizado, guias de instrumentação e códigos de referência utilizados em nossas disciplinas de **Projeto Integrador I e Projetos de Sistemas Úbiquos** do curso de Engenharia de Computação da UFSC, Campus Araranguá.

O objetivo é servir como guia prático para a integração de sensores, calibração de hardware e uso de sistemas operacionais de tempo real.

---

## 🛠️ Ferramentas e Tecnologias

* **Microcontroladores:** ESP32, Família STM32 e arquiteturas ARM Cortex-M.
* **Ambientes de Desenvolvimento:** Zephyr RTOS, Framework Arduino e ESP-IDF.
* **Ferramentas de Software:** VS Code (PlatformIO), CMake e Git.
* **Protocolos de Comunicação:** I2C, SPI, UART e LoRaWAN.


---

## 🔌 Roteiros e Tutoriais: HARDWARE

Guias focados na análise de circuitos, pinagem, níveis de tensão, barramentos físicos e condicionamento de sinal analógico/digital.

### 🌦️ Sensores Ambientais (Projeto Estação Meteorológica)
*   **[Anemômetro - Conexão e Pulso](https://github.com/repositorio-code/2024.1_DEC0013_WEATHER-STATION-HARDWARE/tree/main/sensors/Anemometer):** Instrumentação de sensor de efeito Hall, análise de circuito para contagem de pulsos e proteção de pino contra picos de tensão.
*   **[Sensor BMP280 - Barramento I2C](https://github.com/repositorio-code/2024.1_DEC0013_WEATHER-STATION-HARDWARE/tree/main/sensors/BMP280):** Pinagem do sensor, níveis de tensão de operação (3.3V) e barramento físico I2C com resistores de pull-up.
*   **[Sensor DHT11 - Interface Física](https://github.com/repositorio-code/2024.1_DEC0013_WEATHER-STATION-HARDWARE/tree/main/sensors/DHT11):** Pinagem e requisitos de barramento físico para comunicação em barramento de fio único (Single-Wire).

---

## 💻 Roteiros e Tutoriais: SOFTWARE

Guias focados em lógica de programação, arquitetura de sistemas de tempo real, leitura de protocolos de comunicação e processamento de dados.

### 🫀 Sistemas Operacionais de Tempo Real (RTOS)
*   **[Detecção de Batimentos Cardíacos (Zephyr RTOS)](https://github.com/repositorio-code/2025.2_DEC7562_HEARTBEAT-DETECTION-USING-ZEPHYR-RTOS):** Estruturação do software sob o ecossistema Zephyr. Implementação prática de threads para amostragem do sensor, uso de mutexes para proteção de memória compartilhada e configuração de timers internos.

### 🌦️ Drivers e Leitura de Protocolos
*   **[Leitura I2C - BMP280](https://github.com/repositorio-code/2024.1_DEC0013_WEATHER-STATION-HARDWARE/tree/main/sensors/BMP280):** Implementação de software para varredura de registradores e conversão de dados brutos de pressão e temperatura.
*   **[Protocolo de Comunicação - DHT11](https://github.com/repositorio-code/2024.1_DEC0013_WEATHER-STATION-HARDWARE/tree/main/sensors/DHT11):** Manipulação de software para o sincronismo do sinal de tempo crítico do protocolo Single-Wire.

---

## 🔬 Diretrizes para a Execução dos Experimentos

1. **Validação de Hardware:** Sempre verifique se os níveis lógicos do sensor são compatíveis com o microcontrolador (ex: sensores de 5V em pinos de 3.3V do ESP32/STM32 necessitam de divisor de tensão ou conversor de nível lógico).
2. **Tratamento por Software:** Implemente filtros digitais básicos (como janelas de média móvel) nos códigos para mitigar flutuações e ruídos nas leituras dos pinos analógicos.
