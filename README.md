# 🛡️ K Modbus Scanner: Advanced Modbus TCP Diagnostic Suite / Suíte Avançada de Diagnóstico Modbus TCP 


- [🇺🇸 English Version](#-english-version)
- [🇧🇷 Versão em Português](#-versão-em-português)


---
# 🇺🇸 English Version

> **The ultimate tool for field engineering, commissioning, and Modbus TCP network analysis.**
<img width="1289" height="828" alt="image" src="https://github.com/user-attachments/assets/769b557c-78fb-4648-bda8-874ca6dee4fc" />


**KModbusScanner** is a high-performance desktop application built in Rust, designed for automation professionals who demand more than a simple Modbus client. It combines the agility of a network scanner with the depth of a protocol analyzer and the intelligence of real-time statistics.

![Badge](https://img.shields.io/badge/Status-Project_Ready-success)
![Badge](https://img.shields.io/badge/Language-Rust-orange)
![Badge](https://img.shields.io/badge/UI-egui-blue)

## 🚀 Main Features

### 📡 Topology Scanning
Instantly identify all active devices on your network.
* **ID Scan:** Automatic scanning of Slave IDs (1-247) to locate nodes in gateways or segmented networks.
* **Latency Metrics:** Precise measurement of the response time (RTT) for each device.
* **Connectivity Diagnostics:** TCP port test (SYN Check) before the Modbus connection to avoid unnecessary timeouts.

### 📊 Monitoring and Casting (Polling)
Continuous reading with support for complex data conversion:
* **Supported Functions:** `01` (Coils), `02` (Discrete Inputs), `03` (Holding Registers) and `04` (Input Registers).
* **Data Casting:** Automatic conversion to `UInt16`, `Int16`, and `Float32` (with support for *Big Endian* and *Word Swapped*).
* **Asynchronous Engine:** Multithreaded polling that ensures a fluid interface even in saturated networks.

### 🔎 Memory Search
Locate lost variables or unknown memory maps:
* **Value Search:** Scan address ranges (0-65535) for specific values.
* **Packet Optimization:** Reading up to 124 registers per request for maximum speed.

## 🔬 Deep Diagnostic Zones

### 🛠️ Analyzer Zone: Real-Time Statistics
Transform raw data into operational intelligence.
* **Trend Graphs:** Temporal visualization of multiple variables simultaneously.
* **Statistical Metrics:** Automatic calculations of Minimum, Maximum, Average, and Standard Deviation.
* **Anomaly Detection:**
    * **Outliers:** Automatic identification of out-of-curve values (+3x standard deviation). Calculated from 100 readings.
    * **Stall Detection:** Visual alert when a variable stops updating or "freezes" on the network for more than 100 readings.

### 💻 Nerd Zone: Integrated Packet Sniffer
Inspect byte-level communication without external tools (like Wireshark).
* **Virtual Hex Dump:** Complete visualization of the MBAP Header and PDU.
* **Visual Differentiation:** Clear separation between sent (TX) and received (RX) packets.
* **Analysis:** Identification of transaction IDs and Modbus exception codes natively.

## 📦 Download

For greater agility in the field, **KModbusScanner** is distributed as a portable executable (Single Binary).

[Download](https://github.com/lucaskotres/KModbusScanner/releases/download/1.0.0/KModbusScanner.zip)

> [!IMPORTANT]
> **Total Portability:** The software requires no installation. Just download the `.exe` file and run it directly from any folder or flash drive.

## ⚖️ License and Terms

**Copyright © 2026 Lucas Kotres. All rights reserved.**

This software is provided as a free tool. 
* **Usage:** Permitted for personal and commercial purposes.
* **Redistribution:** Commercial sale or redistribution of the binary or source code is prohibited without prior authorization.
* **Warranty:** The software is provided "as is", without warranty of any kind.
  
❤️ Support the Project

If K Modbus Scanner saved your day in the field or optimized your commissioning time, consider supporting the development.  
Pix(Brazil): 7bbe381a-1ce3-4d69-9d46-f4d844b732fc  or Contact via email at lucaskotres@gmail.com

---

# 🇧🇷 Versão em Português

> **A ferramenta definitiva para engenharia de campo, comissionamento e análise de redes Modbus TCP.**
> <img width="1327" height="818" alt="image" src="https://github.com/user-attachments/assets/45ad2ccd-420f-49ef-955e-3f6f5908aea1" />

O **KModbusScanner** é uma aplicação desktop de alta performance, desenvolvida em Rust, projetada para profissionais de automação que exigem mais do que um simples cliente Modbus. Ele combina a agilidade de um scanner de rede com a profundidade de um analisador de protocolos e a inteligência de estatísticas em tempo real.

![Badge](https://img.shields.io/badge/Status-Project_Ready-success)
![Badge](https://img.shields.io/badge/Language-Rust-orange)
![Badge](https://img.shields.io/badge/UI-egui-blue)

## 🚀 Funcionalidades Principais

### 📡 Varredura de Topologia (Scanning)
Identifique instantaneamente todos os dispositivos ativos em sua rede.
* **Scan por ID:** Varredura automática de Slave IDs (1-247) para localizar nós em gateways ou redes segmentadas.
* **Métricas de Latência:** Medição precisa do tempo de resposta (RTT) de cada dispositivo.
* **Diagnóstico de Conectividade:** Teste de porta TCP (SYN Check) antes da conexão Modbus para evitar timeouts desnecessários.

### 📊 Monitoramento e Casting (Polling)
Leitura contínua com suporte a conversão de dados complexos:
* **Funções Suportadas:** `01` (Coils), `02` (Discrete Inputs), `03` (Holding Registers) e `04` (Input Registers).
* **Data Casting:** Conversão automática para `UInt16`, `Int16`, e `Float32` (com suporte a *Big Endian* e *Word Swapped*).
* **Motor Assíncrono:** Polling multithread que garante interface fluida mesmo em redes saturadas.

### 🔎 Busca de Memória (Search)
Localize variáveis perdidas ou mapas de memória desconhecidos:
* **Busca por Valor:** Vasculhe faixas de endereços (0-65535) por valores específicos.
* **Otimização de Pacotes:** Leitura de até 124 registradores por requisição para máxima velocidade.

## 🔬 Zonas de Diagnóstico Profundo

### 🛠️ Analyzer Zone: Estatísticas em Tempo Real
Transforme dados crus em inteligência operacional.
* **Gráficos de Tendência:** Visualização temporal de múltiplas variáveis simultaneamente.
* **Métricas Estatísticas:** Cálculos automáticos de Mínimo, Máximo, Média e Desvio Padrão.
* **Detecção de Anomalias:**
    * **Outliers:** Identificação automática de valores fora da curva (+3x o desvio padrão). Calculada a partir de 100 leituras.
    * **Stall Detection:** Alerta visual quando uma variável para de atualizar ou "congela" na rede por mais de 100 leituras.

### 💻 Nerd Zone: Sniffer de Pacotes Integrado
Inspecione a comunicação no nível de bytes sem ferramentas externas (como Wireshark).
* **Hex Dump Virtual:** Visualização completa do MBAP Header e PDU.
* **Diferenciação Visual:** Separação clara entre pacotes enviados (TX) e recebidos (RX).
* **Análise:** Identificação de IDs de transação e códigos de exceção Modbus nativamente.

## 📦 Download

Para maior agilidade no campo, o **KModbusScanner** é distribuído como um executável portátil (Single Binary).

[Download](https://github.com/lucaskotres/KModbusScanner/releases/download/1.0.0/KModbusScanner.zip)

> [!IMPORTANT]
> **Portabilidade Total:** O software não requer instalação. Basta baixar o arquivo `.exe` e executá-lo diretamente de qualquer pasta ou pendrive.

## ⚖️ Licença e Termos

**Copyright © 2026 Lucas Kotres. Todos os direitos reservados.**

Este software é fornecido como uma ferramenta gratuita. 
* **Uso:** Permitido para fins pessoais e comerciais.
* **Redistribuição:** Proibida a venda ou redistribuição comercial do binário ou código-fonte sem autorização prévia.
* **Garantia:** O software é fornecido "como está", sem garantias de qualquer tipo.
  
❤️ Apoie o Projeto

Se o K Modbus Scanner salvou seu dia em campo ou otimizou seu tempo de comissionamento, considere apoiar o desenvolvimento.  
Pix: 7bbe381a-1ce3-4d69-9d46-f4d844b732fc - Ou entre em contato pelo email lucaskotres@gmail.com

