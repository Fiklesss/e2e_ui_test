### Описание
Этот проект представляет собой набор автоматизированных тестов 
для проверки функциональности интернет-магазина

### В репозитории содержатся файлы:

- github/workflows
   - run_test.yml - файл конфигурации для выполнения тестов в CI/CD
- base - общие методы, которые используются в pages
- config
    - data.py - загрузка конфиденциальных данных из .env
    - links.py - хранения всех URL-адресов
- pages - описаны локаторы и методы для каждой странице
- tests - содержит тестовые сценарии
- .env - хранение паролей
- conftest.py - настройка веб-драйвера
---

## Ознакомиться с Allure-отчетом:
- Откройте `Action`
- Перейдите в раздел `pages-build-deployment`
- Откройте сгенерированный отчет по ссылке
---

## Запуск теста в GitHub Action:
1. Создайте форк репозитория
2. Создайте токен доступа
    - Перейдите в `Settings` вашего GitHub-аккаунта
    - Перейдите в раздел `Developer settings` > Personal access tokens > Token (classic)
    - Нажмите `Generate new token`, выберите все права и сгенерируйте токен
    - Скопируйте токен
3. Добавьте токен в Secrets проекта
    - Перейдите в `Settings` вашего репозитория
    - В разделе `Secrets` добавьте новый секрет с названием _GH_TOKEN_ и значением вашего сгенерированного токена
4. Создайте ветку (`Branches`) под названием _gh-pages_
5. Запустите Workflow
    - Перейдите во вкладку `Actions` вашего репозитория
    - Выберите workflow с названием `UI-test`
    - Нажмите кнопку `Run` для запуска тестов
    - Дождитесь завершения теста
6. Получите Allure-отчет
    - В Action будет доступен отчет в разделе `pages-build-deployment`
    - Пройдите по предоставленной ссылке для просмотра отчета


