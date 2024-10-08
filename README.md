**Мастерская 2**\
Описние задачи\
Интернет-магазин собирает историю покупателей, проводит рассылки предложений и планирует будущие продажи. Для оптимизации процессов надо выделить пользователей, которые готовы совершить покупку в ближайшее время.\

**Цель**\
Предсказать вероятность покупки в течение 90 дней

**Задачи**

- Изучить данные
- Разработать полезные признаки
- Создать модель для классификации пользователей
- Улучшить модель и максимизировать метрику roc_auc
- Выполнить тестирование

Загружены данные об истории покупателей, истории рекламных рассылок и целевого признака. Выполнена предобработка данных: установлены соответствующие типы данных, удалены дубликаты, значение категорий разбито на 4 отдельных столбца В результате анализа датасетов были добавлены следующие признаки:

- количество купленного товара в разрезе категорий
- сумма выручки от одного клиента
- средня сумма покупки клиента
- разница между первой и последней датой покупки
- число событий по рекламным сообщениям по каждому клитенту
- число рекламных сообщений в разрезе видов
- наиболее часто покупаемые категории товара
- наиболее часто встречающийся идентификатор рассылки

Выполнено обучение модели **CatBoostСlassifier** c GridSearchCV. **Метрика ROC-AUC при тестировании - 0.69**.
