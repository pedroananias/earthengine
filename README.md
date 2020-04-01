# Google Earth Engine (GEE) API for Python: Introdução
# Versão 2

Informações sobre o uso da plataforma Google Earth Engine através da linguagem Python com exemplos explicados em notebooks Jupyter. Reforçamos que os exemplos apresentados neste documento e em seus notebooks foram desenvolvidos com foco em ambientes áquaticos, mas podem ser adaptados para qualquer finalidade.


# Anaconda (Jupyter Notebook - Créditos: Prof. Rogério Galante Negri)

Suíte gratuita que fornece uma série de ferramentas dedicadas às áreas do Aprendizado de Máquina e Ciência de Dados, além de uso geral

- Fazer download da ferramenta em: https://www.anaconda.com/distribution

Porque usar?

- Acesso ao Python
- Acesso à ambientes de desenvolvimento (Jupyther, Visual Studio Code, Spyder, Spyder, PyCharm, etc.)
- Acesso à centenas de bibliotecas/módulos (mais de 1400), dentre eles: Numpy, Matplotlib, SciPy, Scikit-Learn, Pandas e TensorFlow


# Configuração do ambiente em Python

Deve-se instalar as bibliotecas de desenvolvimento necessárias. São sugeridas as seguintes: (Note que a nomenclatura do comando será a mesma para a instalação de qualquer outro pacote que desejar)

1.  Google Earth Engine API - Catálogo de vários petabytes de imagens de satélite e conjuntos de dados geoespaciais com recursos de análise em escala planetária (https://earthengine.google.com): `python -m pip install earthengine-api`
2.  Matplotlib - Criação de gráficos e visualizações de dados em geral (https://matplotlib.org): `python -m pip install matplotlib`
3.  Pandas - Análise e manipulação de dados de código aberto rápida, poderosa, flexível e fácil de usar (https://pandas.pydata.org): `python -m pip install pandas`
4.  Numpy - Suporta arrays e matrizes multidimensionais, possuindo uma larga coleção de funções matemáticas para trabalhar com estas estruturas (https://numpy.org) `python -m pip install numpy`
5.  Requests - Tornar as solicitações HTTP mais simples e mais amigáveis ao ser humano (https://requests.readthedocs.io/en/master): `python -m pip install requests`
6.  Pillow - Adiciona suporte à abertura e gravação de muitos formatos de imagem diferentes (https://pillow.readthedocs.io): `python -m pip install pillow`
7.  Scikit-learn - Aprendizado de máquina de código aberto (https://scikit-learn.org): `python -m pip install sklearn`
8.  Scipy - Feita para matemáticos, cientistas e engenheiros (https://www.scipy.org): `python -m pip install scipy`
9.  Natsort - Classificar listas "naturalmente" (https://pypi.org/project/natsort): `python -m pip install natsort`
10. GeoJSON - Codificando e decodificando dados no formato GeoJSON (https://pypi.org/project/geojson): `python -m pip install geojson`


# Instalação multipacotes

É possível instalar todos os pacotes acima de uma única vez:

`python -m pip install earthengine-api matplotlib pandas numpy requests pillow sklearn scipy natsort geojson`

Existem outras bibliotecas que são sugeridas ao longo do desenvolvimento e serão tratadas nos algoritmos apresentados, mas fazem parte do 'coração' do Python, portanto, não precisam ser instaladas.


# Softwares para desenvolvimento em Python

Abaixo, são listados alguns softwares/ferramentas/IDEs disponíveis para o desenvolvimento em Python:

1.  Jupyter Notebook - Prático e didático! Acompanha a distribuição Ananconda (https://jupyter.org)
2.  Microsoft Visual Studio Code - Em minha opinião, excelente! Gratuíto e com grande varidade de extensões (https://code.visualstudio.com)
3.  PyCharm (https://www.jetbrains.com/pycharm)
4.  Atom (https://atom.io/packages/ide-python)
5.  Google Colab - Um Jupyter Notebook na nuvem! *Necessita conta @unesp.br ou @gmail.com (https://colab.research.google.com)

E tantos outros...um para cada gosto!


# Etapas deste documento e seus arquivos

Orgizamos este documento da seguinte forma, iniciando a conexão com o GEE, até a extração de uma imagem e sua classificação usando machine learning/deep learning.

1.  Primeira conexão com o Google Earth Engine API
2.  Gravando dados em um arquivo de log com a biblioteca 'logging'
3.  Mantendo registro do tempo de execução do algoritmo com a biblioteca 'time'
4.  Coleções, geometrias e filtros: extraindo uma imagem dos datasets do GEE em uma determinada data e local
5.  Indices espectrais: aplicando o NDVI em uma imagem
6.  Utilizando máscaras d'água e nuvem/sombra de nuvem
7.  Extraindo uma imagem PNG do GEE com o Pillow
8.  Transformando uma imagem do GEE em um Dataframe utilizando Reduce Region, Numpy e Pandas
9.  Aplicando um classificador Random Forest em uma imagem e plotando o resultado com o Matplotlib
10. Aplicando um classificador Multi-layer Perceptron em uma imagem e plotando o resultado com o Matplotlib
11. Salvando os pixeis classificados em um geojson com o a biblioteca GeoJSON