# Tópicos em Inteligência Artificial e Otimização

Material dos seminários apresentados na disciplina **Tópicos em Inteligência Artificial e Otimização I** do Programa de Pós-Graduação em Ciência da Computação (PPGCC) da Universidade Federal de Lavras (UFLA).

Cada seminário tem sua própria pasta, com os slides (`.pptx` e `.pdf`) e um notebook Jupyter com as demonstrações práticas.

## Estrutura do repositório

```
topicos-em-ia/
├── I_seminario/
│   ├── Seminário Scikit-learn, PyTorch e Optuna.pptx
│   ├── Seminário Scikit-learn, PyTorch e Optuna.pdf
│   └── Seminário_de_Frameworks_de_IA.ipynb
└── II_seminario/
    ├── Da memória à atenção RNNs, Encoder-Decoder e Transformers.pptx
    ├── Da memória à atenção RNNs, Encoder-Decoder e Transformers.pdf
    └── demos_rnn_transformers.ipynb
```

## I Seminário: Scikit-learn, PyTorch e Optuna

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/flavio-mota/topicos-em-ia/blob/main/I_seminario/Semin%C3%A1rio_de_Frameworks_de_IA.ipynb)

Apresentação de três frameworks de IA usados em sequência para resolver um mesmo problema, do início ao fim: prever o **tipo de cobertura florestal** de uma área de 30 × 30 m a partir de dados cartográficos (base *Covertype*, amostra estratificada de 20.000 linhas, 54 atributos e 7 classes).

| Etapa | Ferramenta | Conteúdo |
|---|---|---|
| 1 | **Scikit-learn** | Escolha do estimador, divisão treino/validação/teste, modelo de referência (`DummyClassifier`), `Pipeline`, validação cruzada e busca em grade com `LinearSVC` |
| 2 | **PyTorch** | Conversão para tensores, rede neural com `nn.Module`, loop de treino escrito à mão e efeito de uma taxa de aprendizado ruim |
| 3 | **Optuna** | Função objetivo, criação e execução do estudo, análise dos *trials* e dos hiperparâmetros encontrados |
| 4 | Síntese | Comparação dos modelos no conjunto de teste e matriz de confusão da rede otimizada |

**Arquivos**

- [Slides (PDF)](I_seminario/Seminário%20Scikit-learn,%20PyTorch%20e%20Optuna.pdf)
- [Slides (PPTX)](I_seminario/Seminário%20Scikit-learn,%20PyTorch%20e%20Optuna.pptx)
- [Notebook](I_seminario/Seminário_de_Frameworks_de_IA.ipynb)

## II Seminário: Da memória à atenção — RNNs, Encoder-Decoder e Transformers

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/flavio-mota/topicos-em-ia/blob/main/II_seminario/demos_rnn_transformers.ipynb)

Evolução das arquiteturas para dados sequenciais, em que cada uma resolve uma limitação da anterior. Todas as demonstrações usam o mesmo problema: **prever as próximas 24 horas de uma série temporal sintética "tipo vento" a partir das últimas 72 horas**.

| Demo | Pergunta | Conteúdo |
|---|---|---|
| 1 | Por que a RNN "esquece"? Como a LSTM resolve? | Decaimento do gradiente ao longo do tempo (RNN × LSTM) e tarefa de memória longa |
| 2 | Como gerar uma *sequência* de saída? | Encoder-Decoder (Seq2Seq) com LSTM, *teacher forcing* e o gargalo do vetor de contexto |
| 3 | O que é atenção, afinal? | Self-attention do zero, escala por √d<sub>k</sub>, codificação posicional, Transformer encoder-decoder pequeno e visualização da cross-attention |

**Arquivos**

- [Slides (PDF)](II_seminario/Da%20memória%20à%20atenção%20RNNs,%20Encoder-Decoder%20e%20Transformers.pdf)
- [Slides (PPTX)](II_seminario/Da%20memória%20à%20atenção%20RNNs,%20Encoder-Decoder%20e%20Transformers.pptx)
- [Notebook](II_seminario/demos_rnn_transformers.ipynb)

## Como executar

A forma mais simples é abrir os notebooks no Google Colab pelos botões acima. Para rodar localmente:

```bash
git clone https://github.com/flavio-mota/topicos-em-ia.git
cd topicos-em-ia
pip install scikit-learn torch optuna pandas numpy matplotlib jupyter
jupyter notebook
```

## Autor

Flávio Mota — PPGCC/UFLA
