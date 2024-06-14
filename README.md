# Clustering KMeans para Dados de Registro de Poço

Este script em Python realiza clustering KMeans em dados de registro de poço usando o formato de arquivo LAS. Ele inclui funcionalidades para pré-processar os dados, determinar o número ótimo de clusters usando o método do cotovelo e o escore de silhueta, aplicar o clustering KMeans, visualizar os clusters e salvar os dados clusterizados em um arquivo CSV.

## Requisitos

Certifique-se de ter os seguintes pacotes Python instalados:
- `lasio`: Para leitura de arquivos LAS.
- `mplstereonet`: Para plotar estereonetes.
- `fracture`: Para análise de fraturas.
- `pandas`, `numpy`: Para manipulação de dados.
- `matplotlib`, `seaborn`: Para plotagem.
- `missingno`: Para visualização de dados faltantes.
- `scikit-learn`: Para clustering KMeans e pré-processamento.
- `yellowbrick`: Para visualizar o método do cotovelo.

Você pode instalar essas dependências usando pip:

```
!pip install lasio mplstereonet fracture pandas numpy matplotlib seaborn missingno scikit-learn yellowbrick
```

## Uso

1. **Links dos Dados:**
   - `well_path`: Link para os dados de registro de poço no formato LAS.
   - `trajectory_path`: Link para dados de trajetória.
   - `fracture_path`: Link para dados de fraturas.

2. **Executando o Script:**
   - Atualize `well_path`, `trajectory_path` e `fracture_path` com seus links de dados reais.
   - Execute o script para realizar o seguinte:
     - Ler dados de registro de poço no formato LAS.
     - Exibir mnemônicos de log.
     - Converter dados para um DataFrame para exibição tabular.
     - Realizar clustering KMeans nos dados de registro de poço selecionados (`well_df2` neste exemplo).
     - Visualizar clusters e opcionalmente salvar o gráfico.
     - Salvar os dados clusterizados em um arquivo CSV.
     - Exibir os primeiros registros dos dados clusterizados.

3. **Classe `KMeansClustering`:**
   - Esta classe encapsula o processo de clustering.
   - Métodos incluem pré-processamento de dados, encontrar o número ótimo de clusters, aplicar KMeans, plotar clusters e salvar dados.

4. **Exemplo:**
   - Um exemplo de uso é fornecido para clusterizar um log específico (`CALI`, neste caso).
   - Modifique o exemplo para se adequar aos seus dados e requisitos específicos.

## Arquivos

- `cluster_plot_DTC.png`: Gráfico salvo dos clusters.
- `clustered_DTC.csv`: Arquivo CSV contendo os dados clusterizados.

## Notas

- Certifique-se de que seus dados estão limpos e tratados para lidar com valores ausentes antes de aplicar o clustering.
- Ajuste parâmetros como `max_clusters` conforme seus dados e requisitos de clustering.
