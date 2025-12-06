# SophonDownloader
Скачивает библиотеки и саму игру от mihoyo через новый метод

[Русский][p:ru-ru] | [中文][p:zh-cn]

---

После того как Genshin сменил SophonChunks, то они обновили и перестали выдавать архивированные файлы начиная с версии 5.6, после этого стало невозможно скачать старые версии игры с библиотеками через оффициальный лаунчер HoYoPlay.

---

# Скачать

* Последний автоматический билд доступен [здесь](https://nightly.link/FlatiCommunity/SophonDownloader/workflows/build/master/Sophon.Downloader.zip) ✨

---

# Как это использовать?
```
Использование:
    Sophon.Downloader.exe full <gameId> <package> <version> <outputDir> [options]                     Download full game assets
    Sophon.Downloader.exe update <gameId> <package> <updateFrom> <updateTo> <outputDir> [options]     Download update assets

Аргументы:
    <gameId>        ID игры, либо hoyo id (hk4e, hkrpg, nap, bh2) или REL id - зашифрованный (gopR6Cufr3, ...)
    <package>       Что конкретно надо скачивать, либо "game" или для аудио "zh-cn", "en-us", "ja-jp" или "ko-kr"
    <version>       Версия игры для скачивания
    <updateFrom>    Если обновляем игру, то с какой версии
    <updateTo>      Если обновляем игру, то до какой версии
    <outputDir>     Директорая куда это всё будет скачено, лучше указывайте через кавычки, имхо пробелы выдадут еррор

Настройки:
    --region=<значение>            Регион игры, которые юзеры используют, либо OSREL (За границей относительно Китая) или CNREL (Китай), по умолч. - OSREL
    --branch=<значение>            Ветка игры для данных, если не шарите про запросы на дедики mihoyo, то игнорьте, обычно у них это main, вродь как есть тестовые, но я по запросам их не видел
    --launcherId=<значение>        ID лаунчера используемого для запроса packages с серваков
    --platApp=<значение>           Тип платформы ID-шником с которой запрашиваем packages
    --threads=<значение>           Количество потоков процессора, по умолч. - парсит ваш процессор и пишет их сюда
    --handles=<значение>           Количество дескрипторов HTTP, по умолч. - 128
    --silent                       Скрытое выполнение сообщений и логирования скачивания (лучше не врубать, а поагентить)
    -h, --help                     Показывает инфу об этом на Английском
```

## Пример использование
```cmd
# Скачать GI версии 6.1.0 только игровые данные с директорией куда это будет распаковано и 128 дескрипторами HTTP
Sophon.Downloader.exe full hk4e game "D:/games/GI/6.1.0/"
```

---

# ID игр

| Игра | ID |
| - | - |
| Honkai Impact 3rd | `bh2` |
| Genshin Impact | `hk4e` |
| Honkai: Star Rail | `hkrpg` |
| Zenless Zone Zero | `nap` |

---

# Заметка (изменена)

Автор делал это в спешке после произошедшего описанного в начале, но после некоторого времени начались ошибки с загрузкой чанков (см. [репорт ошибок на гитхабе](https://github.com/Escartem/SophonDownloader/issues/3)) и умные люди форкающие репос пофиксили всё через переписку загрузчика.

---

# Авторы

- [Hi3Helper.Sophon](https://github.com/CollapseLauncher/Hi3Helper.Sophon) - Sophon assets management
- [MVDW-Java/SophonDownloader](https://github.com/MVDW-Java/SophonDownloader) - Форкер который [пофиксил ошибку](https://github.com/Escartem/SophonDownloader/issues/3)

[p:ru-ru]: README.md
[p:zh-cn]: README_zh-cn.md