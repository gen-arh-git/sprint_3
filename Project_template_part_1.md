
# Задание 1. Анализ и планирование

Чтобы составить документ с описанием текущей архитектуры приложения, можно часть информации взять из описания компании условия задания. Это нормально.

### 1. Описание функциональности монолитного приложения

**Управление отоплением:**

- Пользователи могут управлять отоплением в своих домах дистанционно.
- Система поддерживает физические реле и устройства, что позволяет управлять котлами.

**Мониторинг температуры:**

- Пользователи могут получить актуальную температуру 
- Система поддерживает заросы температуры от датчиков

### 2. Анализ архитектуры монолитного приложения

- Язык программирования: Java
- База данных: PostgreSQL
- Архитектура: Монолитная, все компоненты системы (обработка запросов, бизнес-логика, работа с данными) находятся в рамках одного приложения.
- Взаимодействие: Синхронное, запросы обрабатываются последовательно.
- Масштабируемость: Ограничена, так как монолит сложно масштабировать по частям.
- Развёртывание: Требует остановки всего приложения.
- Количестов клиентов: 100 

### 3. Определение доменов и границы контекстов

1. Управление пользователями. Регистрация, авторизация и предоставление доступа
2. Управление устройствами. Регистрация и управление устройствами
3. Телеметрия устройств. Сбор даных с устройств для аналитики и информирования.

### **4. Проблемы монолитного решения**

- Масштабирование. В условиях возрастающей нагрузки на определённые сервисы не представляется возможным расширить его функциональные возможности
- Отказоустойчивость. Вследствие сбоя в работе одного из компонентов системы может произойти полное её обрушение
- Разработка. При увеличении объема разработки релизный цикл станет единым для всех команд. Это означает, что все будут ждать и согласовывать между собой процедуру релиза.
- Команда. В крупных коллективах работа над единым проектом нередко сопровождается возникновением разногласий и промедлением.

### 5. Визуализация контекста системы — диаграмма С4

[Диаграмма контекста в модели C4](./puml/1_Context_C4.puml)

# Задание 2. Проектирование микросервисной архитектуры

В этом задании вам нужно предоставить только диаграммы в модели C4. Мы не просим вас отдельно описывать получившиеся микросервисы и то, как вы определили взаимодействия между компонентами To-Be системы. Если вы правильно подготовите диаграммы C4, они и так это покажут.

**Диаграмма контейнеров (Containers)**

[Диаграмма  контейнеров (Containers)](./puml/2_Container_C4.puml)

**Диаграмма компонентов (Components)**

[Диаграмма компонентов (Components](./puml/3_Component_С4.puml)

**Диаграмма кода (Code)**

[Диаграмма кода (Code)](./puml/4_Code_C4.puml)

# Задание 3. Разработка ER-диаграммы

[ER-диаграмма](./puml/ER_diagram.puml)
