# Solution Summary

## 1. Exploratory Data Analysis (EDA)
**Notebook: 00_first_small_eda.ipynb**
- Загружены и исследованы исходные данные.
- Рассмотрены всевозможные постановки задач
- Выполнено первичное изучение данных, включая распределение текстов по длине.
- Построены гистограммы длины текстов и частотного распределения слов.
- Была сделана гипотеза о выбросах по длине, которая не подтвердилась

## 2. Data Cleaning & Lemmatization
**Notebook: 01_cleaning_lemmatization.ipynb**
- Выполнена предобработка текстов: удаление пунктуации, цифр, стоп-слов.
- Была решена задача NER, необходимая для эффективной замены именнованных сущностей на токены.
- Применена лемматизация для приведения слов к нормальной форме.
- Проведена визуализация наиболее частых слов после очистки данных.
- Былы сделан фичи инжинеринг для числовьх фичей.

## 3. Clustering Analysis
**Notebook: 02_process_embedding.ipynb**
- Использованы методы кластеризации (K-Means, DBSCAN) для группировки текстов.
- Оптимизировано количество кластеров с помощью метода локтя.
- Тексты преобразованы в векторное представление с использованием TF-IDF и FastText.
- Рассчитаны косинусные расстояния между текстами для выявления схожести.
- Визуализированы embeddings с помощью PCA и t-SNE.
  

## 4. Topic Modeling with LDA
**Notebook: 04_topic_modelling_with_lda.ipynb**
- Применена модель латентного размещения Дирихле (LDA) для выделения тем.
- Определено оптимальное количество тем с использованием перплексии и когерентности.
- Визуализированы ключевые слова для каждой темы с помощью `pyLDAvis`.
- Выявлены основные тематические группы, характерные для текстов.

## 5. -  ABSA
**Notebooks 5  and later ....**
- из полученных данных с предыдущих ноутбуков следует, что задачу надо рассматривать как ABSA ( aspect based sentiment analyses)
- 200 случайно выбранных сэмплов были размечены  с использованием gpt-4,  как оценщика, показали точность и полноту 100% на 5 случайно выбранных примерах.
- была сделана сделана попытка обучить deepseek 7b используя промпт тьюнинг, но она не паказала хороший результат.


## Key Insights
- В одном отзыве, и даже в предложении часто содержится много семантических топиков, поэтому стандартные алгоритмы, которые векторизуют сразу весь документ, не справляются.
- Векторы embeddings от разных моделей  не могут рассположить тексты так, чтобы при ручном просмотре было интуитивно понятно, что они разбиты на класстеры.
- Использование тематического моделирования с LDA позволяет нащупать определенные кластеры, но все равно встречается много общих слов.
- Решение задачи как ABSA с GPT-4 показал отличный результат.


## Next Steps
- Обучить открытыю модель на английском датасете задачи ABSA, а потом инферить русские предложения, через анлийский переводчик
- Обучить открытую модель на русском языке задачи ABSA.

---


