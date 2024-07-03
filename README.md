## **Проект 4. Модель Предсказания Вероятности Открытия Депозита в Банке**

## Оглавление
1. [Описание Проекта](README.md#описание-проекта)
2. [Основные Задачи](README.md#основные-задачи)
3. [Краткая Информация о Данных](README.md#краткая-информация-о-данных)
4. [Этапы Работы над Проектом](README.md#этапы-работы-над-проектом)
5. [Результат](README.md#результат)


### Описание Проекта

Банки хранят огромные объёмы информации о своих клиентах. Эти данные можно использовать для того, чтобы оставаться на связи с клиентами и индивидуально ориентировать их на подходящие именно им продукты или банковские предложения.

Обычно с выбранными клиентами связываются напрямую через разные каналы связи: лично (например, при визите в банк), по телефону, по электронной почте, в мессенджерах и так далее. Этот вид маркетинга называется прямым маркетингом. На самом деле, прямой маркетинг используется для взаимодействия с клиентами в большинстве банков и страховых компаний. Но, разумеется, проведение маркетинговых кампаний и взаимодействие с клиентами — это трудозатратно и дорого.

Банкам хотелось бы уметь выбирать среди своих клиентов именно тех, которые с наибольшей вероятностью воспользуются тем или иным предложением, и связываться именно с ними.

Вам предоставили данные о последней маркетинговой кампании, которую проводил банк: задачей было привлечь клиентов для открытия депозита. Вы должны проанализировать эти данные, выявить закономерность и найти решающие факторы, повлиявшие на то, что клиент вложил деньги именно в этот банк. Если вы сможете это сделать, то поднимете доходы банка и поможете понять целевую аудиторию, которую необходимо привлекать путём рекламы и различных предложений.

:arrow_up:[to Table of Contents](README.md#оглавление)


### Основные Задачи

*Бизнес-задача*: определить характеристики, по которым можно выявить клиентов, более склонных к открытию депозита в банке, и за счёт этого повысить результативность маркетинговой кампании.

*Техническая задача*: построить модель машинного обучения, которая на основе предложенных характеристик клиента будет предсказывать, воспользуется он предложением об открытии депозита или нет.

_Основные цели_:
1. Исследовать данные;
2. Выявить характерные черты для потенциальных клиентов, чтобы чётко очертить ЦА и увеличить прибыль банка;
3. Использовать разные инструменты для повышения качества прогноза.

:arrow_up:[to Table of Contents](README.md#оглавление)


### Краткая Информация о Данных

Данные о клиентах банка:

        age (возраст);
        job (сфера занятости);
        marital (семейное положение);
        education (уровень образования);
        default (имеется ли просроченный кредит);
        housing (имеется ли кредит на жильё);
        loan (имеется ли кредит на личные нужды);
        balance (баланс).

Данные, связанные с последним контактом в контексте текущей маркетинговой кампании:

        contact (тип контакта с клиентом);
        month (месяц, в котором был последний контакт);
        day (день, в который был последний контакт);
        duration (продолжительность контакта в секундах).

Прочие признаки:

        campaign (количество контактов с этим клиентом в течение текущей кампании);
        pdays (количество пропущенных дней с момента последней маркетинговой кампании до контакта в текущей кампании);
        previous (количество контактов до текущей кампании)
        poutcome (результат прошлой маркетинговой кампании).

И целевая переменная deposit, которая определяет, согласится ли клиент открыть депозит в банке.

:arrow_up:[to Table of Contents](README.md#оглавление)


### Этапы Работы над Проектом

1. Описательный Анализ Данных:
   - знакомство с данными

2. Обработка Данных:
   - работа с пропусками и выбросами в данных
   - удаление признаков

3. Преобразование Данных:
   - работа с пропусками
   - создание признаков
   - кодировка признаков

4. Разведывательный Анализ Данных:
   - Проверка на Мультиколлинеарность:
      - Pearson's Correlation для числовых признаков
   - Визуализация Данных:
      - исследовать данные
      - нащупать первые закономерности и выдвинуть гипотезы

5. Очистка и Отбор Признаков:
   - преобразование и удаление признаков
   - отбор признаков на основании мультиколлинеарности и с помощью метода KBest

6. Построение Моделей:
   - разделение данных для модели: выделение обучаемой и тестовой частей
   - подбор метрик для оченки качества

7. Обучение Моделей для Решения Задачи Классификации:
   - логистическая регрессия
   - деревья решений
   - случайный лес
   - gradient boosting
   - stacking

:arrow_up:[to Table of Contents](README.md#оглавление)


### Результат

В результате лучшие результаты показали модели:

    - GridSearch + Random Forest: F1-Score = 0.811
    - Random Forest: F1-Score = 0.818
    - Gradient Boosting: F1-Score = 0.817


:arrow_up:[to Table of Contents](README.md#оглавление)
