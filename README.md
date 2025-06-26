# Geração de Sinais de ECG Sintéticos para Aumento de Dados

Este repositório contém artigos e materiais de pesquisa relacionados à geração de sinais de eletrocardiograma (ECG) sintéticos utilizando modelos de aprendizado de máquina. O objetivo principal é explorar técnicas de *data augmentation* para melhorar as métricas de classificação de arritmias cardíacas em bancos de dados desbalanceados.

## Artigos de Pesquisa

Os artigos neste repositório detalham o uso de diferentes modelos generativos e suas aplicações na classificação de sinais de ECG.

### 1. Classificação de Sinais de ECG Sintéticos

* [cite_start]**Autores:** Eduardo P. L. Jaqueira, Renato Candido e Magno T. M. Silva[cite: 15, 16].
* [cite_start]**Evento:** XLII Simpósio Brasileiro de Telecomunicações e Processamento de Sinais (SBrT 2024), de 01 a 04 de outubro de 2024, em Belém, PA[cite: 1].
* [cite_start]**Resumo:** Este artigo apresenta a geração de sinais de ECG sintéticos usando dois modelos generativos: uma Rede Adversária Generativa (GAN) e um Autocodificador Variacional (VAE)[cite: 1, 5]. [cite_start]Os sinais sintéticos foram classificados por uma rede perceptron multicamada (MLP) treinada com sinais reais, resultando em uma taxa de acerto superior a 80%, o que sugere a utilidade desses sinais para melhorar a classificação de arritmias cardíacas[cite: 2, 3, 6, 7]. [cite_start]O estudo focou na geração de batimentos da classe N (batimentos do nó sinoatrial) do banco de dados MIT-BIH Arrhythmia Database (MITDB), a classe mais representativa[cite: 12, 18, 36].
* **Modelos Utilizados:**
    * [cite_start]**GAN (Generative Adversarial Network):** O gerador usa uma rede neural recorrente bidirecional com blocos BiLSTM, e o discriminador é uma rede MLP com seis camadas ocultas[cite: 22, 26, 28]. [cite_start]A taxa de aproveitamento dos sinais gerados foi de 26,5%[cite: 40].
    * [cite_start]**VAE (Variational Autoencoder):** O codificador e o decodificador são redes MLP[cite: 30]. [cite_start]A taxa de aproveitamento dos sinais gerados foi de 8,8%[cite: 40].
* [cite_start]**Resultados Principais:** A rede MLP obteve uma taxa de acerto de 85% para os sinais gerados pela GAN e cerca de 81% para os sinais do VAE[cite: 43]. [cite_start]A GAN demonstrou melhor "qualidade" nos sinais sintéticos, mas o VAE teve um tempo de treinamento e custo computacional cerca de cinco vezes menor[cite: 49, 50].

### 2. Geração de ECG Sintético com Autocodificador Variacional

* [cite_start]**Autores:** Eduardo P. L. Jaqueira, Renato Candido e Magno T. M. Silva[cite: 63].
* [cite_start]**Evento:** 32º Simpósio Internacional de Iniciação Científica e Tecnológica da USP (SIICUSP 2024)[cite: 62].
* [cite_start]**Resumo:** Este trabalho utiliza um autocodificador variacional (VAE) para gerar sinais de ECG sintéticos[cite: 64]. [cite_start]A inclusão desses sinais sintéticos no conjunto de treinamento de uma rede perceptron multicamada (MLP) resultou em uma melhoria na taxa de acerto da rede para a classificação de arritmias cardíacas[cite: 65, 66]. [cite_start]O foco deste estudo preliminar foi gerar sinais da classe S (supraventriculares ectópicos) do banco de dados MITDB[cite: 77, 78].
* [cite_start]**Métodos:** Um VAE foi utilizado para gerar os sinais, sendo o codificador e o decodificador compostos por redes MLP[cite: 68, 69]. [cite_start]O treinamento do VAE considerou uma combinação do erro quadrático médio e da divergência de Kullback-Leibler como função de custo[cite: 69]. [cite_start]Seis "templates" foram selecionados como representantes da classe S para verificar a variabilidade dos sinais[cite: 81]. [cite_start]Sinais gerados com uma distância DTW (dynamic time warping) acima de um limiar foram descartados[cite: 79, 86].
* [cite_start]**Resultados Principais:** A expansão do banco de dados com sinais sintéticos da classe S resultou em uma melhora na taxa de acerto para a classe S (de 11% para 13%), classe N (de 78% para 80%), e classe F (de 3,2% para 11%)[cite: 83, 89]. [cite_start]A inclusão dos dados sintéticos reduziu significativamente o erro de classificação de sinais da classe S como pertencentes à classe F, passando de 9% para 0,5%[cite: 90, 91]. [cite_start]Isso demonstra o benefício do aumento de dados para a taxa de acerto da rede MLP[cite: 92].

## Próximos Passos (Trabalhos Futuros)

Ambos os artigos indicam direções para pesquisas futuras:
* [cite_start]Gerar sinais sintéticos para as classes menos representativas (como S, V e F) a fim de balancear o banco de dados por completo[cite: 19, 52, 94].
* [cite_start]Retreinar a rede MLP com um banco de dados sintético balanceado e validar os resultados com dados reais[cite: 53].
* [cite_start]Explorar configurações do VAE que possam levar a resultados de qualidade semelhantes aos da GAN, considerando o menor custo computacional do VAE[cite: 51].
* [cite_start]Utilizar um modelo mais robusto para a geração de sinais e encontrar formas de gerar sinais mais variados dentro de uma mesma classe[cite: 93].

## Financiamento

Este trabalho foi financiado pelas seguintes agências de fomento:
* [cite_start]CAPES (código de financiamento 001) [cite: 17]
* [cite_start]CNPq (127301/2023-2, 303826/2022-3 e 404081/2023-1) [cite: 17]
* [cite_start]FAPESP (2021/02063-6) [cite: 17]
