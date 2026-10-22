# DuckDeck hbmenu

Публичный форк [switchbrew/nx-hbmenu](https://github.com/switchbrew/nx-hbmenu), основанный на v3.6.1 (`fd26270a4e4b6994886a57b0738d98229ab4094e`).

Локальные изменения Jeronimo701: сетка приложений с настройкой числа столбцов и размера иконок через `config/nx-hbmenu/duckdeck.cfg`, скруглённые иконки, панель выбранного приложения, навигация и сенсорный выбор в сетке. Изменены `common/menu.c`, `common/menu.h`, `nx_main/main.c`, `nx_main/nx_touch.c`.

Лицензия исходного hbmenu и модификаций — ISC, см. LICENSE.md. Исходная история и авторство сохранены. Этот перенос публикует исходники; проверка на физической Switch и готовый релиз не выполнялись.

## Документация исходного проекта

### Usage
See [Homebrew_Applications](https://switchbrew.org/wiki/Homebrew_Applications) for SD layout and applications, etc. See [Switchbrew](https://switchbrew.org/wiki/Homebrew_Menu) for hbmenu docs.

### Download
The latest release is available from the [releases](https://github.com/switchbrew/nx-hbmenu/releases/latest) page.

### Building
Build for the Nintendo Switch with ```make nx``` and for the PC with ```make pc```.
Running ```make``` builds for both systems.

The following [pacman packages](https://devkitpro.org/wiki/devkitPro_pacman) are required to build for Switch:
- `switch-dev`
- `switch-freetype`
- `switch-libconfig`
- `switch-libjpeg-turbo`
- `switch-physfs`

The following libraries are required to build for PC:
- `libfreetype`
- `libconfig`
- `libjpeg-turbo`
- `libphysfs`
- `sdl2`

Building for Switch/PC requires `zip`.

Since C11 threads are used, building for the PC may fail if C11 threads are not available.

#### Credits

* This uses code based on 3DS [new-hbmenu](https://github.com/fincs/new-hbmenu).
* `libjpeg-turbo` is used for handling JPEG icons. This library doesn't support lossless JPEG (likewise for official sw which uses `libjpeg-turbo`).
* `c11threads` is used for implement C11 Threads on Windows and macOS.