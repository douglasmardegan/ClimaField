# ClimaField: Estação metereológica IoT 

[![Status do Projeto](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow)](#)
[![Hardware](https://img.shields.io/badge/Hardware-ESP32-blue)](#)
[![Área](https://img.shields.io/badge/Foco-Agricultura%20de%20Precis%C3%A3o-green)](#)
[![Linguagem](https://img.shields.io/badge/Linguagem-C++-orange)](#)
[![Licença](https://img.shields.io/badge/Licen%C3%A7a-Propriet%C3%A1ria-red)](#)

[English Version](README.en.md) | Versão em Português

## 📌 Sobre o projeto
O **ClimaField** é uma estação meteorológica de baixo custo e alta precisão. Construído sobre a plataforma ESP32 (C++), o projeto não apenas realiza a leitura de sensores, mas processa as informações localmente (*Edge Computing*) para entregar métricas prontas para a tomada de decisão no campo.

A união da engenharia eletrônica com a ciência agronômica permite que o equipamento atue como uma ferramenta crítica para a agricultura de precisão, fornecendo dados vitais para o manejo hídrico e para a segurança e eficácia das operações de campo.

## 🌱 Relevância agronômica
Os dados coletados e processados por esta estação têm aplicação direta em operações agrícolas avançadas:
* **Janelas de pulverização:** O cálculo embutido do *ponto de orvalho* e o monitoramento da umidade são fundamentais para calcular o *Delta T*, métrica essencial para otimizar aplicações de defensivos (especialmente as realizadas por drones e aeronaves agrícolas), mitigando riscos de deriva e evaporação rápida das gotas.
* **Prevenção e controle de doenças:** O monitoramento contínuo de temperatura e umidade relativa ajuda na modelagem de alertas para doenças fúngicas.
* **Análise termodinâmica:** Os dados de pressão atmosférica auxiliam na previsão de frentes frias e chuvas locais com maior assertividade do que grandes modelos meteorológicos regionais.

## 🚀 Roadmap e futuras implementações
- [x] Leitura base de temperatura, umidade e pressão atmosférica.
- [x] Processamento na borda: Cálculo matemático do ponto de orvalho por meio da equação de Magnus-Tetens.
- [ ] **Expansão de sensores:** Integração de anemômetro e pluviômetro de báscula.
- [ ] **Telemetria IoT:** Envio de dados via protocolo MQTT para dashboards remotos.
- [ ] **Integração de dados:** Estruturação de pipelines (ex: Python) para análise espacial do microclima e integração com ferramentas GIS.
- [ ] **Alimentação autônoma:** Implementação de painel solar com gerenciador de carga (TP4056) para operação ininterrupta no campo.

## ⚖️ Licença e direitos autorais
**© 2026 Douglas Mardegan Colodete. Todos os direitos reservados.**

Este projeto é **proprietário**. O material aqui disponibilizado (documentação, esquemáticos, lógicas de funcionamento e demonstrações visuais) tem como único objetivo a apresentação técnica para portfólio profissional. 

É **estritamente proibida** a cópia, reprodução, distribuição, modificação ou utilização (comercial ou pessoal) de qualquer parte deste projeto, hardware ou firmware sem a autorização prévia e expressa por escrito do autor. 

> *Nota: Por se tratar de propriedade intelectual protegida, o código-fonte integral não está disponível para clonagem pública.*

