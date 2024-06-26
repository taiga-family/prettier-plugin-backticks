<img src="./images/banner.webp" alt="prettier-plugin-backticks" />

# prettier-plugin-backticks

`prettier-plugin-backticks` — это плагин для Prettier, многопрофильного форматировщика кода, который автоматически
заменяет кавычки в ваших файлах JavaScript или TypeScript на обратные кавычки. Этот плагин идеально подходит для
разработчиков, которые предпочитают использовать обратные кавычки вместо одинарных или двойных кавычек для строк в своем
коде, обеспечивая единообразный стиль по всему проекту.

## Особенности

- Конвертирует все одинарные и двойные кавычки в обратные кавычки (`) в файлах JavaScript и TypeScript с некоторыми исключениями.
  1. Выражение "use strict", которое не заменяется для сохранения точного синтаксического значения.
  2. Ключи объекта, где использование одинарных или двойных кавычек является необходимым для сохранения имен ключей, содержащих символы, не допускаемые без кавычек.
  3. Строки в инструкциях import и require, чтобы не нарушать синтаксис модулей.
  4. Строки в инструкции по объявлению модуля, чтобы не нарушать синтаксис модулей.
  5. (Временно) Строки в инструкциях динамического импорта, из-за того, что некоторые среды разработки некорректно обрабатывают такие импорты, если они заключены в обратные кавычки.
  6. (Временно) Строки в селекторах для компонентов Angular из-за того, что некоторые среды разработки некорректно обрабатывают такие селекторы, если они заключены в обратные кавычки.

## Установка

Вы можете установить `prettier-plugin-backticks` через npm или yarn. Сначала убедитесь, что у вас установлен Prettier
в вашем проекте. Если нет, установите Prettier:

```bash
npm install --save-dev prettier
# или
yarn add --dev prettier
```

Затем установите `prettier-plugin-backticks`:

```bash
npm install -D @taiga-ui/prettier-plugin-backticks
# или
yarn add --dev @taiga-ui/prettier-plugin-backticks
```

Затем добавьте плагин в ваш файл `.prettierrc`:

```json
{
  "plugins": ["@taiga-ui/prettier-plugin-backticks"]
}
```

## Использование

После установки `prettier-plugin-backticks` вы можете запустить Prettier, как обычно. Например, чтобы отформатировать
все файлы в вашем проекте, выполните:

```bash
npx prettier --write .
# или
yarn prettier --write .
```

## Совместимые плагины

* `@trivago/prettier-plugin-sort-imports`
