# Компания - repetit.ru (проектная занятость)
# Должность - Специалист по Data Science 
#  Описание задачи

Построение ML-продукта для оптимизации классификации заявок на оплату для сервиса Repetit.ru
сервис Repetit.ru работает с большим количеством заявок от клиентов с данными о предмете, желаемой стоимости, возрасте ученика, целью занятий и тд. К сожалению, 7 из 8 не доходят до оплаты, при этом обработка заявки консультантом увеличивает конверсию в оплату на 30%. 

проблема в том, что консультантов не хватает на все заявки и получается, что чем больше заявок — тем меньше конверсия из заявки в оплату и консультанты тратят время на бесперспективные заявки.

разработал модель, которая по имеющейся информации о клиенте и заявке будет предсказывать вероятность оплаты заявки клиентом. Заказчик хочет понять, какие заявки будут оплачены, а какие нет, чтобы одни обрабатывать вручную консультантами, а другие нет. Оценка качества модели будет производиться с использованием precision и ROC-AUC. 

для решения даной задачи:

- выполнил предобработку: выявил и удалил аномалии, дубли, удалил пропуски
- создал целевой признак на основе имеющихся значений
- объединил датасеты, т.о. добавив каждой заявке признаки
- создал новые признаки
- обучил (с учетом дисбаланса классов) ML модели: CatBoostClassifier, RandomForestClassifier, DecisionTreeClassifier, LogisticRegression
- выявил наиболее важные признаки

в результате получил ML-модель, основанную на CatBoostClassifier и решающую указанную задачу

pandas, matplotlib, sklearn(RandomForestClassifier, DecisionTreeClassifier, LogisticRegression, train_test_split, StandardScaler), catboost
