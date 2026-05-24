# Структура дашборда DataLens

## Общая логика дашборда

Дашборд состоит из трёх страниц:

1. `Общий обзор`
2. `Временные паттерны`
3. `Типы слушателей`

Структура дашборда соответствует исследовательской задаче проекта: анализу пользовательской активности, временных паттернов прослушивания и итоговой классификации пользователей.

## Страница 1. Общий обзор

### Основные таблицы

- `listenings_datalens.csv`
- `listening_sessions.csv`

### Элементы страницы

- KPI: всего прослушиваний
- KPI: количество пользователей
- KPI: количество активных дней
- KPI: количество сессий
- линейный график прослушиваний по датам
- столбчатый график прослушиваний по часам
- столбчатый график прослушиваний по дням недели

### Фильтры

- `username`
- `date_only`
- `day_part`
- `weekend`


## Страница 2. Временные паттерны

### Основные таблицы

- `listenings_datalens.csv`
- `user_daily_activity.csv`
- `user_weekday_hour_profile.csv`

### Элементы страницы

- распределение прослушиваний по частям суток
- сводная таблица `weekday x hour`
- сравнение будней и выходных
- график активности пользователей по дням
- таблица по `active_days` и `avg_daily_plays`

### Фильтры

- `username`
- `day_part`
- `weekday`
- `weekend`

## Страница 3. Типы слушателей

### Основные таблицы

- `user_features.csv`
- `user_activity_types.csv`

### Элементы страницы

- распределение пользователей по `listener_type`
- распределение пользователей по `behavior_profile`
- точечный график: `active_days_share x avg_daily_plays`
- точечный график: `night_share x weekend_share`
- таблица пользователей со следующими полями:
  - `username`
  - `listener_type`
  - `behavior_profile`
  - `active_days_share`
  - `avg_daily_plays`
  - `night_share`
  - `evening_share`
  - `weekend_share`
  - `session_count`
  - `avg_session_length`

### Фильтры

- `listener_type`
- `behavior_profile`
- `username`
