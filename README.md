# 🛡️ ModSkan: Suíte Avançada de Diagnóstico Modbus TCP

> **A ferramenta definitiva para engenharia de campo, comissionamento e análise forense de redes industriais.**

O **ModSkan** é uma aplicação desktop de alta performance, desenvolvida em Rust, projetada para profissionais de automação que exigem mais do que um simples cliente Modbus. Ele combina a agilidade de um scanner de rede com a profundidade de um analisador de protocolos e a inteligência de estatísticas em tempo real.

![Badge](https://img.shields.io/badge/Status-Project_Ready-success)
![Badge](https://img.shields.io/badge/Language-Rust-orange)
![Badge](https://img.shields.io/badge/UI-egui-blue)

---

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

### 🔎 Busca Forense de Memória (Blind Search)
Localize variáveis perdidas ou mapas de memória desconhecidos:
* **Busca por Valor:** Vasculhe faixas de endereços (0-65535) por valores específicos.
* **Otimização de Pacotes:** Chunking inteligente que lê até 124 registradores por requisição para máxima velocidade.

---

## 🔬 Zonas de Diagnóstico Profundo

### 🛠️ Analyzer Zone: Estatísticas em Tempo Real
Transforme dados crus em inteligência operacional.
* **Gráficos de Tendência:** Visualização temporal de múltiplas variáveis simultaneamente.
* **Métricas Estatísticas:** Cálculos automáticos de Mínimo, Máximo, Média e Desvio Padrão.
* **Detecção de Anomalias:**
    * **Outliers:** Identificação automática de valores fora da curva (3σ).
    * **Staller Detection:** Alerta visual quando uma variável para de atualizar ou "congela" na rede.

### 💻 Nerd Zone: Sniffer de Pacotes Integrado
Inspecione a comunicação no nível de bits sem ferramentas externas (como Wireshark).
* **Hex Dump Virtual:** Visualização completa do MBAP Header e PDU.
* **Diferenciação Visual:** Separação clara entre pacotes enviados (TX) e recebidos (RX).
* **Análise Forense:** Identificação de IDs de transação e códigos de exceção Modbus nativamente.

---

## 🛠️ Requisitos e Instalação

### Pré-requisitos
* **Rust Toolchain:** [Instalar Rust](https://rustup.rs/) (Versão estável mais recente).
* **Windows Dependencies:** Garantir que o `Visual C++ Build Tools` esteja instalado.

### Compilação
```powershell
# Clone o repositório
git clone https://github.com/lucaskotres/KotresModbusScanner2.git
cd KotresModbusScanner2

# Execute o projeto em modo release
cargo run --release
```

---

## ⚖️ Licença e Termos

**Copyright © 2026 Lucas Kotres. Todos os direitos reservados.**

Este software é fornecido como uma ferramenta gratuita para uso profissional e de campo. 
* **Uso:** Permitido para fins pessoais e comerciais.
* **Redistribuição:** Proibida a venda ou redistribuição comercial do binário ou código-fonte sem autorização prévia.
* **Garantia:** O software é fornecido "como está", sem garantias de qualquer tipo.

---

> [!TIP]
> **Dica Pro:** Utilize a porta 502 como padrão, mas lembre-se que alguns equipamentos industriais podem utilizar portas personalizadas configuráveis no Painel de Conexão.
