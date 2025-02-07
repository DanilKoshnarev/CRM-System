# CRM System

## Описание
CRM System - это приложение для управления взаимоотношениями с клиентами, которое позволяет управлять контактами, отслеживать взаимодействия и создавать отчеты.

## Структура проекта
Проект разделен на несколько слоев для улучшения читаемости и поддерживаемости кода:

- **Domain**: Основная бизнес-логика и правила.
- **Application**: Интерфейсы, юзкейсы и реализации для работы с данными.
- **Infrastructure**: Реализация деталей инфраструктуры, таких как модели данных, контроллеры и утилиты.
- **Presentation**: Визуализация данных и взаимодействие с пользователем.

## Установка
1. Клонируйте репозиторий:
    ```bash
    git clone <URL репозитария>
    ```
2. Перейдите в каталог проекта:
    ```bash
    cd crm
    ```
3. Соберите проект с помощью Maven:
    ```bash
    mvn clean install
    ```

## Запуск
Для запуска проекта выполните команду:
```bash
mvn exec:java -Dexec.mainClass="com.example.crm.Application"
```

## Структура каталогов
```plaintext
crm/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── com/
│   │   │   │   └── example/
│   │   │   │       └── crm/
│   │   │   │           ├── domain/
│   │   │   │           │   ├── entities/
│   │   │   │           │   │   ├── Contact.java
│   │   │   │           │   │   └── Interaction.java
│   │   │   │           │   ├── repositories/
│   │   │   │           │   │   └── ContactRepository.java
│   │   │   │           │   ├── services/
│   │   │   │           │   │   └── ContactService.java
│   │   │   │           │   └── usecases/
│   │   │   │           │       └── ManageContact.java
│   │   │   │           ├── infrastructure/
│   │   │   │           │   ├── models/
│   │   │   │           │   │   └── ContactModel.java
│   │   │   │           │   ├── controllers/
│   │   │   │           │   │   └── ContactController.java
│   │   │   │           ├── Application.java
│   │   └── resources/
│   │       └── application.properties
│   ├── test/
│       └── java/
│           └── com/
│               └── example/
│                   └── crm/
│                       └── ApplicationTests.java
├── pom.xml
└── README.md
```

## Описание компонентов
### Domain
- **Contact.java**: Класс сущности контакта.
- **Interaction.java**: Класс сущности взаимодействия.
- **ContactRepository.java**: Интерфейс репозитория контактов.
- **ContactService.java**: Сервис для управления контактами.

### Application
- **ManageContact.java**: Юзкейс для управления контактами.

### Infrastructure
- **ContactModel.java**: Модель данных контакта.
- **ContactController.java**: Контроллер для управления контактами.

### Presentation
- **ContactView.java**: Представление для отображения контактов.

## Лицензия
Этот проект лицензирован под лицензией MIT. Для получения дополнительной информации см. файл LICENSE.
