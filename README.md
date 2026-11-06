# ⚡ Voltímetro USB & Testador de Carga

Uma aplicação Android moderna desenvolvida em **Kotlin** e **Jetpack Compose (Material 3)** para medir em tempo real a potência exata ($\text{Watts}$, $\text{Volts}$ e $\text{Amperes}$) que o telefone está a receber de qualquer carregador ou porta USB. 

Desenvolvida especialmente para ajudar a comparar e identificar qual o melhor carregador ou qual a porta USB do carro que carrega mais rápido.

---

## ✨ Funcionalidades Principais

1. **📊 Leitura Instantânea & Estável (Filtro EMA)**
   - Medição em tempo real de **Tensão ($\text{V}$)**, **Corrente ($\text{mA}$ / $\text{A}$)** e **Potência ($\text{W}$)**.
   - Aplica um filtro de Média Móvel Exponencial (EMA) para eliminar o ruído elétrico dos sensores e fornecer leituras estáveis e sem saltos bruscos.
   - **Índice de Estabilidade do Sinal ($\%$)** para avaliar a qualidade e pureza da energia fornecida pelo carregador.

2. **🚦 Classificação Inteligente da Velocidade de Carga**
   - Identificação automática e com código de cores:
     - ⚡ **Carga Rápida** ($> 12\text{W}$ ou $> 2200\text{mA}$)
     - 🔋 **Carga Normal** ($5\text{W} - 12\text{W}$)
     - 🐢 **Carga Lenta** ($< 5\text{W}$)
     - 🔌 **A Descarregar / Bateria Cheia**

3. **🏁 Benchmark Automatizado de 10 Segundos (Porta A vs Porta B)**
   - Ferramenta dedicada para testar e comparar portas USB (ex: Portas do Automóvel).
   - Mede durante 10 segundos a estabilidade e potência média de cada porta e **declara automaticamente a vencedora** com a percentagem de ganho de velocidade.

4. **⏳ Tempo Estimado até 100%**
   - Estimativa dinâmica do tempo restante até carga completa da bateria baseada na taxa real de carregamento.

5. **🔍 Aba de Diagnóstico Inteligente & Suporte**
   - Análise local de temperatura, estado de saúde da bateria e possíveis problemas de carregamento.
   - **Botões de Suporte**:
     - **Doar (1€)**: Círculo branco com "1€" e pop-up informativo com link para doação via PayPal (`paypal.me/manelitomartins/1`).
     - **Sugestões**: Círculo branco com "i" de igual tamanho com link direto para formulário de feedback do Google Forms.

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem**: Kotlin (`2.2.10`)
- **UI Framework**: Jetpack Compose & Material 3
- **Arquitetura**: MVVM (Model-View-ViewModel) com Coroutines & StateFlow
- **APIs do Sistema**: `BatteryManager` (`ACTION_BATTERY_CHANGED`, `BATTERY_PROPERTY_CURRENT_NOW`, `computeChargeTimeRemaining`)

---
