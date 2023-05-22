# Технічне завдання

## Огляд проєкту
Проєкт має на меті реалізацію сторніки з сіткою ігор згідно наданого макету.
Макет - https://www.figma.com/file/6OwFVTyKuv59H2b3cdE9jW/Untitled?type=design&node-id=1%3A539&t=ab5UlGbhKM4kS8IU-1

## Вимоги

1. *Використання Nuxt 3:* Проєкт повинен бути реалізований з використанням фреймворку Nuxt 3. Версія фреймворку повинна бути сумісна з останнім стабільним випуском.
2. *Доступність з публічного репозиторію:* Проєкт має бути опублікований в публічном репозиторії GitHub або GitLab.
4. *Дані про ігри:* Дані про ігри надані у форматі JSON в файлі `games.json`. Необхідно засобами Nuxt реалізувати api ендпоїнт який віддаватиме список ігор.
5. *Логотипи ігор:* Згідно з макетом на кожній карточці має відображатись логотип цієї гри. Логотопи розташрвані в архіві `logos.zip`, імʼя файла відповідає id гри.
6. *Чистота кода:* Сітка ігор повинна бути розбита на компоненти для легшої керованості та перевикористання коду. Компоненти повинні бути розроблені згідно з найкращими практиками та забезпечувати чистоту коду.
7. *Адаптивний дизайн:* Сітка ігор повинна бути адаптивною та коректно відображатися на різних розмірах екранів, включаючи мобільні пристрої, планшети та настільні комп’ютери. На макеті відображені варіанти сітки на різних екранах.
8. *Пошук за назвою гри або назвою провайдера:* Користувач повинен мати можливість ввести пошуковий запит, і сітка ігор повинна
   відфільтрувати та відобразити лише картки ігор, які відповідають пошуковому запиту. Фільтрація відбувається як по назві самої гри (поле `title`) так і по назві ігрового провайдера (поле `provider`).
   
## Додаткові вимоги (бонусні бали)
*  *Конфігурація ESlint:* Для забезпечення чистоти коду бажано додати наступні плагіни в конфігурацію ESlint:
```
   {
      "extends": [
        "eslint:recommended",
        "plugin:nuxt/recommended",
        "plugin:vue/vue3-recommended",
        "@vue/eslint-config-airbnb",
        "plugin:tailwindcss/recommended" // please add if using tailwind
      ]
    }
```

* *Реалізація додаткових станів:* У компоненті сітки ігор потрібно реалізувати додаткові стани, яких немає на наданому
  макеті. Ці стани включають:
    * *Стан завантаження:* Коли дані про ігри завантажуються з сервера, потрібно відображати стан завантаження, який повідомляє користувача про процес завантаження даних. Це може бути анімація завантаження, спеціальний індикатор або будь-який інший спосіб візуального відображення стану завантаження.
    * *Стан відсутності результатів:* Якщо результати пошуку не знайдено або відповідні ігри відсутні, потрібно відобразити відповідний стан відсутності результатів. Це може бути повідомлення, що ігри не знайдено або відповідний візуальний елемент, який вказує на відсутність результатів.
