# 🌦️ ClimaField: Estação metereológica IoT 

[![Status do Projeto](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow)](#)
[![Hardware](https://img.shields.io/badge/Hardware-ESP32-blue)](#)
[![Área](https://img.shields.io/badge/Foco-Agricultura%20de%20Precis%C3%A3o-green)](#)
[![Linguagem](https://img.shields.io/badge/Linguagem-C++-orange)](#)

[English Version](README.en.md) | Versão em Português

## 📌 Sobre o Projeto
A **ClimaField** é uma estação meteorológica de baixo custo e alta precisão, desenvolvida para o monitoramento de microclimas agrícolas na borda da lavoura. Construído sobre a plataforma ESP32 (C++), o projeto não apenas realiza a leitura de sensores, mas processa as informações localmente (*Edge Computing*) para entregar métricas prontas para a tomada de decisão no campo.

A união da engenharia eletrônica com a ciência agronômica permite que o equipamento atue como uma ferramenta crítica para a agricultura de precisão, fornecendo dados vitais para o manejo hídrico e para a segurança e eficácia das operações de campo.

## 🌱 Relevância Agronômica
Os dados coletados e processados por esta estação têm aplicação direta em operações agrícolas avançadas:
* **Janelas de Pulverização:** O cálculo embutido do Ponto de Orvalho e o monitoramento da umidade são fundamentais para calcular o *Delta T*, métrica essencial para otimizar aplicações de defensivos (especialmente as realizadas por drones agrícolas), mitigando riscos de deriva e evaporação rápida das gotas.
* **Prevenção de Doenças:** O monitoramento contínuo de temperatura e umidade relativa ajuda na modelagem de alertas para doenças fúngicas.
* **Análise Termodinâmica:** Os dados de pressão atmosférica auxiliam na previsão de frentes frias e chuvas locais com maior assertividade do que grandes modelos meteorológicos regionais.

## ⚙️ Arquitetura e Hardware
* **Microcontrolador:** ESP32 (Permite futura integração IoT via Wi-Fi/Bluetooth)
* **Sensores Atuais:**
  * **DHT22:** Temperatura e Umidade Relativa do ar.
  * **BMP280:** Pressão Atmosférica e Temperatura secundária.

### 🔌 Esquema de Ligação (Pinout)
| Componente | Pino do Sensor | Pino no ESP32 | Observação |
| :--- | :--- | :--- | :--- |
| **DHT22** | VCC / GND | 3V3 / GND | Utilizar resistor pull-up de 10kΩ no pino de dados |
| | DATA | GPIO 4 | |
| **BMP280** | VCC / GND | 3V3 / GND | Comunicação via barramento I2C |
| | SCL | GPIO 22 | SCL Padrão do ESP32 |
| | SDA | GPIO 21 | SDA Padrão do ESP32 |

## 🚀 Roadmap e Futuras Implementações
- [x] Leitura base de Temperatura, Umidade e Pressão Atmosférica.
- [x] Processamento na borda: Cálculo matemático do Ponto de Orvalho (Magnus-Tetens).
- [ ] **Expansão de Sensores:** Integração de Anemômetro (velocidade do vento) e Pluviômetro de báscula.
- [ ] **Telemetria IoT:** Envio de dados via protocolo MQTT para dashboards remotos.
- [ ] **Integração de Dados:** Estruturação de pipelines (ex: Python) para análise espacial do microclima e integração com ferramentas GIS.
- [ ] **Alimentação Autônoma:** Implementação de painel solar com gerenciador de carga (TP4056) para operação ininterrupta no campo.

## 🛠️ Como Executar
1. Clone este repositório.
2. Na Arduino IDE, instale as bibliotecas: `DHT sensor library` e `Adafruit BMP280`.
3. Carregue o firmware `AgroMeteo.ino` para o ESP32.
4. Abra o Monitor Serial em `115200 baud` para acompanhar as leituras ambientais.
