# Classificador-SVM
### Descrição
Treinando um modelo de classificação utilizando support vector machines, aplicando em uma base de dados para classificar registros e compartilhar os resultados(Censo de 1994 - EUA).

O objetivo é prever se uma pessoa possui renda anual <= ou > 50 mil dólares por ano.

**Percentual mínimo a ser batido** -> Base Line Classifier = 0.7559 (ZeroR).

### Resultados - Validação Cruzada - StratifiedKFold
**Precisão** | **Pré-Processamentos** | **Desvio Padrão**
| :------: | :------: | :------: |
? | LabelEncoder | ?
? | OneHotEncoder | ?
0.8146 | LabelEncoder + StandardScaler | 0.0078
**0.8513** | **OneHotEncoder + StandardScaler** | **0.0058**
0.8513 | LabelEnconder + OneHotEncoder + StandardScaler | 0.0058

**?** = Não aplicar escalonamento dos dados (StandardScale) faz com que o processamento se torne extremamente lento, inviável.

### Matriz de Confusão (Média):
**x** | 0 | 1
| :------: | :------: | :------: |
0 | **2315.9** | 156.1
1 | 327.8 | **456.3**

A Matriz na tabela acima é formada pela média de todas as matrizes geradas ao longo de 10 execuções usando pré-processamentos OneHotEncoder + StandardScaler.

A diagonal principal (em negrito) destaca os registros classificados corretamente.

### Especificações dos parâmetros usados:
- SVC(kernel = 'linear', random_state = 1)

### Bibliotecas usadas:
- Pandas
- Sklearn
- Numpy

### Ferramentas Usadas:
- Anaconda
- Spyder

### Fonte da Base de Dados: 
- Dua, D. and Graff, C. (2019). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

### Como usar:
1. Faça o download do classificador já treinado dispoível neste mesmo repositório [aqui](https://github.com/juliomrodrigues/Classificador-SVM/blob/main/classificador_svm.sav).
2. Abra o arquivo.py que deseja usar o classificador ou então crie um novo.
3. Execute o código abaixo para fazer a importação:
~~~~python
import pickle
classificador_svm = pickle.load(open('classificador_svm.sav', 'rb'))

~~~~~
4. Pronto, agora o classficador está pronto para ser usado.
5. Se desejar treinar um novo classificador, faça o download do arquivo de treinamento e execute novas combinações de pré-processamentos e parâmetros [aqui](https://github.com/juliomrodrigues/Classificador-SVM/blob/main/treinamento_classificador_svm.py).

#### Outros Classificadores:
- [Naive Bayes](https://github.com/juliomrodrigues/Classificador-Naive-Bayes)
- [Árvore de Decisão](https://github.com/juliomrodrigues/Arvore-de-Decisao)
- [Random Forest](https://github.com/juliomrodrigues/Random-Forest-Classificador)
- [Aprendizagem por Regras](https://github.com/juliomrodrigues/Classificador-Regras)
- [Aprendizagem por Instâncias(KNN)](https://github.com/juliomrodrigues/Classificador-KNN)
- [Regressão Logística](https://github.com/juliomrodrigues/Regressao-Logistica-Classificador)
- [Rede Neural](https://github.com/juliomrodrigues/Classificador-Rede-Neural)
