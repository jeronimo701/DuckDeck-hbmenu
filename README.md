# DuckDeck hbmenu

Homebrew-меню для Nintendo Switch с сеткой приложений вместо стандартной ленты. Можно выбрать число столбцов и размер иконок; поддерживается навигация кнопками и сенсорный выбор.

**Форк nx-hbmenu 3.6.1 · Nintendo Switch · ISC**

[Скачать предварительную сборку](https://github.com/jeronimo701/DuckDeck-hbmenu/releases/tag/v3.6.1-duckdeck-20261022) · [Сборка](BUILD-RELEASE.ru.md) · [Исходный проект](https://github.com/switchbrew/nx-hbmenu) · [Проблемы](https://github.com/jeronimo701/DuckDeck-hbmenu/issues)

## Чем отличается от nx-hbmenu

- Сетка приложений с настраиваемыми столбцами.
- Скруглённые иконки и панель выбранного приложения.
- Навигация и сенсорный выбор, адаптированные к сетке.
- Настройки в `config/nx-hbmenu/duckdeck.cfg` на SD.

Скриншот с физической Switch пока не добавлен: готовая сборка есть, но запуск на консоли отдельно не проверен. Изображение чужого меню вместо DuckDeck здесь не используется.

## Как попробовать

1. Сохрани текущий `hbmenu.nro` и резервную копию SD на ПК.
2. Скачай `DuckDeck-hbmenu.nro` из [релиза](https://github.com/jeronimo701/DuckDeck-hbmenu/releases/tag/v3.6.1-duckdeck-20261022).
3. Для стандартного способа запуска hbmenu используй копию как `hbmenu.nro` в корне SD. Способ запуска зависит от твоей CFW.
4. По желанию создай `config/nx-hbmenu/duckdeck.cfg`:

```text
duckdeck = {
    columns = 4;
    iconSize = 96;
};
```

Столбцы: **1–6**, размер иконок: **48–256**. По умолчанию — 4 столбца и 96 px. Это предварительная сборка: держи исходный hbmenu под рукой для возврата.

## Сборка

Нужны devkitPro/devkitA64, libnx и зависимости, перечисленные в [DETAILS.ru.md](DETAILS.ru.md). Команда для Switch:

```sh
make nx TARGET=DuckDeck-hbmenu APP_VERSION=3.6.1-duckdeck-20261022
```

Готовый NRO и его заголовки проверены при подготовке сборки. Запись на SD и тест на реальной консоли этим не подтверждаются. [Протокол](BUILD-RELEASE.ru.md).

## Авторство

Основан на [switchbrew/nx-hbmenu](https://github.com/switchbrew/nx-hbmenu) v3.6.1, коммит `fd26270a4e4b6994886a57b0738d98229ab4094e`. Изменения сетки — **Jeronimo701**. История и авторство upstream сохранены.

Код и модификации — [ISC](LICENSE.md), сторонние компоненты — [THIRD-PARTY.md](THIRD-PARTY.md). Это не официальный продукт Nintendo.
