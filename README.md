# TA2 — Modelagem do Canal Rádio Móvel (AWGN + Desvanecimento Rayleigh)

Trabalho acadêmico da disciplina **Comunicações Digitais**: modelagem de uma comunicação de telemetria em **canal gaussiano (AWGN)** com **desvanecimento Rayleigh**, utilizando simulação computacional.

## Integrantes
- Grupo: `Equipe 8`

## Organização do repositório
- `SImulacao.ipynb`  
  Simulação de transmissão/receptor com **modulação BPSK**, canal **Rayleigh** e ruído **AWGN**, com cálculo de **BER**.

- `SRARG_equipe_8.ipynb`  
  Geração e visualização das variáveis aleatórias (Uniforme, Rayleigh, Gaussiana), curvas de **probabilidade de erro (BER)**, **vazão** e análise de **correlação**.

- `PREMISSAS DO PROJETO SIMULAÇÃO.pdf`  
  Enunciado e premissas do trabalho.

- `Parte analítica e detalhamento_fluxograma/`  
  Materiais da fundamentação teórica e imagens do fluxograma/diagrama do sistema.

## Fundamentação do modelo
### Bits transmitidos (fonte)
O sinal de transmissão é baseado em bits:
- **bit 0 → tx = -1**
- **bit 1 → tx = +1**

### Modulação
- **BPSK**: mapeamento dos bits para símbolos reais em \{-1, +1\}.

### Canal
- **AWGN** (Additive White Gaussian Noise): ruído gaussiano aditivo.
- **Desvanecimento Rayleigh**: multiplicação do sinal por um coeficiente aleatório (fading Rayleigh), modelando flutuações do canal.

### Receptor
- Combinação de canal e detecção (decisão por limiar) para reconstrução dos bits.
- **BER** calculado comparando bits transmitidos vs. bits detectados.

## Fluxograma e diagrama do sistema
(usar as figuras do material disponibilizado)

- Diagrama de blocos:
  `Parte analítica e detalhamento_fluxograma/Diagrama-de-blocos-de-um-sistema-de-comunicacao.png`

- Fluxograma detalhado:
  `Parte analítica e detalhamento_fluxograma/Detalhamento_Fluxograma.png`

## Experimentos e resultados esperados
Os notebooks foram estruturados para gerar:

### 1) Histogramas (variáveis aleatórias)
- Histograma da **Variável Aleatória Uniforme**
- Histograma da **Variável Aleatória Rayleigh**
- Histograma da **Variável Aleatória Gaussiana**

### 2) Curvas de BER vs. Eb/N0
- **AWGN sem Rayleigh**
- **AWGN + Rayleigh**

> Os gráficos e comparações (simulado vs. teórico, quando aplicável) ficam dentro dos notebooks.

### 3) Vazão na camada física
- Vazão **sem erro**
- Vazão **com erro (AWGN)**

### 4) Correlação
- Visualização dos efeitos do ruído e do desvanecimento no sinal recebido, incluindo situações em que o erro ocorre na detecção.

## Como executar
> Observação: os gráficos e resultados são gerados ao rodar as células dos notebooks. Não é necessário editar o código para obter as figuras.

### Requisitos (ajustar se necessário)
- Python 3.x
- `numpy`
- `matplotlib`
- `scipy`

### Passo a passo
1. Abra `SImulacao.ipynb` ou `SRARG_equipe_8.ipynb`
2. Rode as células na ordem
3. Use as figuras geradas para compor o relatório e a apresentação

## Entrega (conforme premissas do trabalho)
- Relatório: incluir introdução/fundamentação teórica/resultados/conclusões/referências
- Apresentação: baseada na fundamentação e no detalhamento do fluxograma/diagrama
- As curvas solicitadas devem ser obtidas pelas simulações dos notebooks

