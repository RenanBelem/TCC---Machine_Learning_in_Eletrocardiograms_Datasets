#Investigação de Anomalias Cardíacas em Datasets de Eletrocardiogramas> **Projeto de Conclusão de Curso (TCC)** > **Curso:** Ciência da Computação - PUCPR
> **Autores:** Henrique L. Richa, Renan B. Biavati, Vitória Izabel M. Pinto
> <img width="544" height="460" alt="image" src="https://github.com/user-attachments/assets/688f2be7-31fd-4da9-923e-8a9585ad7505" />


##📋 Sobre o Projeto Este projeto explora a aplicação de técnicas de **Aprendizado de Máquina (Machine Learning)** na análise de eletrocardiogramas (ECG), com o objetivo de automatizar e aprimorar a detecção de anomalias cardíacas.

Diante da complexidade dos dados de ECG, o estudo compara diversos algoritmos de aprendizado supervisionado para identificar padrões no **MIT-BIH Arrhythmia Database**, maximizando métricas críticas como acurácia e especificidade.

##🎯 Objetivos* Comparar a eficácia de diferentes modelos de ML na classificação de batimentos cardíacos.
* Otimizar hiperparâmetros utilizando **GridSearch** para refinar os resultados.


* Implementar técnicas avançadas de **Ensemble (Stacking)** para superar o desempenho de modelos isolados.

##🗃️ Base de DadosO projeto utiliza o **MIT-BIH Arrhythmia Database** (https://www.kaggle.com/datasets/shayanfazeli/heartbeat), um padrão-ouro para pesquisas de arritmia.

* 
**Classes Analisadas:** O dataset possui 5 classes principais de batimentos (Normal, Supraventricular, Ventricular, Fusão, Inclassificável).


* 
*Nota:* O *PTB Diagnostic ECG Database* foi analisado, mas excluído do escopo final devido à incompatibilidade de classes para junção direta.



##🚀 Tecnologias e BibliotecasO projeto foi desenvolvido em **Python** utilizando **Jupyter Notebooks**.

* **Manipulação de Dados:** `pandas`, `numpy`
* **Visualização:** `matplotlib`, `seaborn`
* **Machine Learning:** `scikit-learn`
* **Modelos Avançados:** `xgboost`
* **Ensemble:** `vecstack`
* **Serialização:** `joblib`

##🧠 Modelos ImplementadosForam desenvolvidos e avaliados 7 modelos individuais e 1 estratégia de Stacking:

1. 
**KNN (K-Nearest Neighbors)** 


2. 
**SVM (Support Vector Machine)** 


3. 
**Random Forest** 


4. 
**MLP (Multilayer Perceptron)** 


5. 
**AdaBoost** 


6. 
**Gradient Boosting** 


7. 
**XGBoost** 


8. 
**Stacking (Ensemble)**: Combinação das previsões dos modelos acima.



##📂 Estrutura do RepositórioOs arquivos estão organizados conforme a etapa de experimentação:

| Arquivo | Descrição |
| --- | --- |
| `experimentacao_knn.ipynb` | Treinamento e otimização do KNN. |
| `experimentacao_svm.ipynb` | Treinamento e otimização do SVM. |
| `experimentacao_randomforest.ipynb` | Treinamento e otimização do Random Forest. |
| `experiementacao_mlp.ipynb` | Treinamento e otimização da Rede Neural MLP. |
| `experiementacao_adaboost.ipynb` | Treinamento e otimização do AdaBoost. |
| `experimentacao_gradientboost.ipynb` | Treinamento e otimização do Gradient Boosting. |
| `experimentacao_xgboost.ipynb` | Treinamento e otimização do XGBoost. |
| `experimentacao_stacking4.ipynb` | **Modelo Final:** Estratégia de Stacking (Meta-modelo XGBoost) utilizando os melhores classificadores base. |
| `Artigo Científico.pdf` | Documentação teórica completa e análise detalhada dos resultados. |

##📊 Resultados ChaveOs modelos passaram por rigorosa otimização de hiperparâmetros. Abaixo, os destaques dos resultados otimizados (Média Ponderada):

| Modelo | Acurácia | F1-Score | Especificidade |
| --- | --- | --- | --- |
| **XGBoost** | **98.0%** | **98.0%** | **98.44%** |
| SVC | 98.0% | 98.0% | 98.0% |
| KNN | 97.7% | 97.6% | 97.6% |
| MLP Classifier | 97.1% | 97.0% | 97.8% |
| GradientBoost | 97.0% | 97.0% | 96.8% |
| Random Forest | 97.0% | 96.5% | 96.8% |
| AdaBoost | 89.0% | 87.0% | 88.8% |

> 
> **Destaque:** O **XGBoost** apresentou o melhor desempenho individual. A estratégia de **Stacking (Experimento 4)**, utilizando o melhor modelo como meta-modelo, demonstrou superioridade sobre estratégias que utilizavam modelos mais fracos como decisores.
> 
> 

##⚙️ Como Executar1. **Instale as dependências:**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost vecstack tabulate joblib

```


2. **Dataset:** Certifique-se de que os arquivos `mitbih_train.csv` e `mitbih_test.csv` estejam no mesmo diretório dos notebooks.
3. **Execução:**
* Execute os notebooks `experimentacao_<modelo>.ipynb` individualmente para ver o treinamento e a geração dos arquivos `.joblib`.
* Execute `experimentacao_stacking4.ipynb` para rodar o ensemble final.



---

###📝 Citação
Se utilizar este trabalho ou parte dele, favor citar:

> Richa, H. L.; Biavati, R. B.; Pinto, V. I. M. (2024). *Investigação de Anomalias Cardíacas em Datasets de Eletrocardiogramas*. Pontifícia Universidade Católica do Paraná (PUCPR). 
> 
> 

---
