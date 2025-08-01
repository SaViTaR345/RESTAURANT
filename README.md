# Restaurant Management System

## Описание приложения

Приложение "Restaurant Management System" - это система управления рестораном, разработанная на C# с использованием Windows Forms и PostgreSQL. Система предоставляет функционал для трех типов пользователей:

1. **Посетители (Visitors)**:
   - Просмотр меню
   - Бронирование столиков
   - Создание заказов
   - Просмотр истории заказов

2. **Официанты (Waiters)**:
   - Управление заказами
   - Подтверждение оплаты
   - Освобождение столиков
   - Просмотр текущих бронирований

3. **Администраторы (Admins)**:
   - Управление меню
   - Управление пользователями
   - Просмотр отчетов
   - Настройки системы

Приложение автоматически проверяет и освобождает столики с истекшим временем бронирования при каждом запуске.

## Установка и настройка

1. **Скачивание и распаковка**:
   - Скачайте архивный файл (RAR) с проектом
   - Распакуйте его в удобное место на вашем компьютере

2. **Настройка базы данных**:
   - Откройте pgAdmin4
   - Выберите свою базу данных (или создайте новую)
   - Кликните правой кнопкой мыши на базе данных
   - Выберите "Restore..."
   - В диалоговом окне выберите файл `restoranee.sql` из распакованной папки
   - Нажмите "Restore" для импорта структуры базы данных и тестовых данных

3. **Настройка подключения**:
   - Откройте проект в Visual Studio (файл `WinFormsAPP1.sln`)
   - Найдите класс `DatabaseConnection.cs`
   - Измените параметры подключения к БД (сервер, имя базы данных, логин и пароль) на свои

4. **Запуск приложения**:
   - Нажмите F5 или кнопку "Start" в Visual Studio
   - Приложение запустится с формой входа

## Функциональные особенности

1. **Автоматическое освобождение столиков**:
   - При каждом запуске система проверяет бронирования
   - Столики с истекшим временем бронирования автоматически освобождаются
   - Бронирования помечаются как "Expired"

2. **Гибкая система ролей**:
   - Три уровня доступа (посетитель, официант, администратор)
   - Возможность регистрации с кодами доступа для официантов и администраторов

3. **Управление заказами**:
   - Полный цикл от создания до оплаты
   - Автоматическое освобождение столиков после оплаты
   - Логирование всех операций

4. **Удобный интерфейс**:
   - Раздельные формы для разных ролей
   - Интуитивно понятное управление
   - Визуализация данных в таблицах

## Технические требования

- Windows 7/10/11
- .NET Framework 4.7.2 или выше
- PostgreSQL 12+
- pgAdmin 4+
- Visual Studio 2019/2022 (для разработки)

## Дополнительные возможности

Система может быть легко расширена для добавления:
- Управления инвентарем
- Генерации отчетов
- Интеграции с платежными системами
- Системы лояльности для клиентов
