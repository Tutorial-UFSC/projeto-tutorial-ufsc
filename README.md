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

## 📁 Links para os Tutoriais e Laboratórios

Os códigos e roteiros estão divididos pelos módulos de desenvolvimento abaixo:

### 🌦️ Módulo: Sensores e Aquisição de Dados (Estação Meteorológica)
Desenvolvimento focado em leitura de barramentos digitais e tratamento de sinal analógico.

*   **[Anemômetro](https://github.com/repositorio-code/2024.1_DEC0013_WEATHER-STATION-HARDWARE/tree/main/sensors/Anemometer):** Contagem de pulsos e integração de sensor de efeito Hall para medição de velocidade do vento.
*   **[Sensor BMP280](https://github.com/repositorio-code/2024.1_DEC0013_WEATHER-STATION-HARDWARE/tree/main/sensors/BMP280):** Leitura de pressão atmosférica e temperatura via barramento I2C.
*   **[Sensor DHT11](https://github.com/repositorio-code/2024.1_DEC0013_WEATHER-STATION-HARDWARE/tree/main/sensors/DHT11):** Coleta de umidade e temperatura utilizando protocolo Single-Wire (fio único).

### 🫀 Módulo: Sistemas de Tempo Real (RTOS)
Aplicações focadas em determinismo, gerência de tarefas e instrumentação médica.

*   **[Detecção de Batimentos Cardíacos (Zephyr RTOS)](https://github.com/repositorio-code/2025.2_DEC7562_HEARTBEAT-DETECTION-USING-ZEPHYR-RTOS):** Implementação de monitoramento cardíaco utilizando threads, mutexes e timers no ecossistema Zephyr.

---

## 🔬 Diretrizes para os Experimentos

Para a execução dos laboratórios, recomenda-se seguir o seguinte roteiro de validação:

1. **Análise de Hardware:** Verificação de pinagem, níveis de tensão (3.3V/5V) e resistores de pull-up necessários no barramento (I2C/Single-Wire).
2. **Filtragem de Sinal:** Implementação de filtros digitais simples (como média móvel) para estabilização das leituras dos sensores em ambientes com ruído.
3. **Depuração:** Validação do status de inicialização dos periféricos via monitor serial antes de integrar os módulos de conectividade.

---

## 🎓 Uso Acadêmico e Contribuições

Este portal é um ambiente vivo e colaborativo. Se você identificar melhorias nas rotinas de filtragem dos sensores, encontrar alguma inconsistência nos pinos dos diagramas ou quiser propor novas implementações (como suporte a novos RTOS), sinta-se à vontade para abrir uma **Pull Request** ou registrar uma **Issue** no repositório correspondente.
