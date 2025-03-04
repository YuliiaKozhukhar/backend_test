# Тестове завдання на позицію Backend розробника

## Технічні вимоги
- Використовувати лише стандартні компоненти Laravel 10
- Команда і ендпоінт мають бути покриті тестами
- Результат має містити README з описом як його розгорнути

## Функціональні вимоги

- Тестове завдання повинно працювати використовуючи наданий docker-compose (додайте необхідні контейнери)
- Написати клас клієнт для зовнішнього АРІ ([Документація з АРІ](api.md))
- Клас клієнту має бути використоватись як DI контейнер і може бути заміненим іншим класом
- Написати команду яка буде парсити дані за допомогою клієнту і зберігати їх в базу даних (створіть необхідну структуру БД)
- Написати метод який буде віддавати дані про компаніі. Вимоги до ендпоінту:
  - підтримка пагінації
  - можливість пошуку за назвою компанії/адресою або її частиною

Приклад відповіді
```json
{
  "data":[
    {
      "id":"1ee15eed-6baa-4732-afc0-f12c35b7dc25",
      "name":"Mixtape Inc.",
      "address":"1693 Alice Court, Annapolis MD 21401",
      "users":[
        {
          "id":"5a963e9b-ac97-4bd3-94af-64513f4ee3a0",
          "name_last":"Axelroad",
          "name_first":"Robert",
          "email":"b.axelroad@example.com",
          "position":"CEO"
        },
        ...
      ]
    },
    ...
  ],
  ...
}
```


