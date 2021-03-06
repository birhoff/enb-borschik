История изменений
=================

2.4.0
-----

* Модуль `borschik@1.5.3` обновлен до версии `1.6.0`.

2.3.1
-----

* Модуль `borschik@1.5.2` обновлен до версии `1.5.3`: исправлена обработка ошибок для `enb` ([#borschik-112]).

2.3.0
-----

### API

В API пакета добавлено поле `borschik`.

```js
var borschik = require('enb-borschik').borschik;
```

Если на проекте используется `borschik` вместе с `enb-borschik`, то версии `borschik` могут отличаться.

```js
"devDependencies": {
    "enb-borschik": "2.3.0", // использует borschik@1.5.2
    "borschik": "1.5.1"
}
```

Чтобы этого не происходило следует использовать `borschik` из `enb-borschik`.

### Зависимости

* Модуль `borschik@1.5.1` обновлен до версии `1.5.2`:
    * Модуль `csso@1.5.1` обновлен до версии `1.5.4`.

2.2.1
-----

* Модуль `borschik@1.5.0` обновлен до версии `1.5.1`:
    * Модуль `csso@1.4.2` обновлен до версии `1.5.1`.
    * Модуль `uglify-js@2.4.24` обновлен до версии `2.6.1`.
* Модуль `inherit@2.2.2` обновлен до версии `2.2.3`.
* Модуль `vow@0.4.11` обновлен до версии `0.4.12`.

2.2.0
-----

* Модуль `borschik@1.4.1` обновлен до версии `1.5.0`:
    * Модуль `csso@1.3.11` обновлен до версии `1.4.2`.
    * Модуль `uglify-js@2.4.15` обновлен до версии `2.4.24`.
* Модуль `vow@0.4.10` обновлен до версии `0.4.11`.

2.1.0
-----

* Добавлена поддержка `enb` версии `1.x` ([#43]).

2.0.0
-----

### Технологии

* [ __*major*__ ] Технология `css-borschik-chunks` была удалена ([#14], [#38]). Вместо нее следует использовать одноименную технологию из пакета `enb-bembundle`.

#### `borschik`

Технология [borschik](api.ru.md#borschik) была переписана с помощью `build-flow` ([#20]). Кроме того, произошли следующие изменения:

* [ __*major*__ ] [freeze](api.ru.md#freeze) включен по умолчанию и будет работать только при наличии конфигурационного файла `.borschik` ([#37]).
* Добавлена опция [dependantFiles](api.ru.md#dependantfiles) ([#24]). Она необходима для случаев, когда обрабатываемый файл зависит от других собираемых файлов (например, для обработки HTML-файла могут понадобиться CSS- и JS-файлы).
* Для ускорения сборки вместо модуля `sibling` используется [общая очередь дочерних процессов](https://github.com/enb/enb#nodegetsharedresources) ([#32]).

### Зависимости

* [ __*major*__ ] Модуль `borschik@1.3.2` обновлен до версии `1.4.1` и больше не является `peer`-зависимостью.
* [ __*major*__ ] Изменились требования к версии модуля `enb`. Теперь для корректной работы требуется `enb` версии `0.16.0` или выше.
* Модуль `vow@0.4.3` обновлен до версии `0.4.10`.
* Модуль `inherit@2.2.1` обновлен до версии `2.2.2`.

[#borschik-112]: https://github.com/bem/borschik/pull/112
[#43]: https://github.com/enb/enb-borschik/pull/43
[#38]: https://github.com/enb/enb-borschik/issues/38
[#37]: https://github.com/enb/enb-borschik/issues/37
[#32]: https://github.com/enb/enb-borschik/pull/32
[#24]: https://github.com/enb/enb-borschik/issues/24
[#20]: https://github.com/enb/enb-borschik/issues/20
[#14]: https://github.com/enb/enb-borschik/issues/14
