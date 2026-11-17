# Security policy / Политика безопасности

EN <img src="https://flagcdn.com/20x15/us.png" width="20" height="15" alt="US">
## Supported versions
Security fixes are released only for the **latest version** of KrogosLab and of its modules. Please update before reporting: [latest release](../../releases/latest).

## Reporting a vulnerability
Please **do not** open a public issue for a security problem.
Report it privately: **[Security → Report a vulnerability](../../security/advisories/new)** in this repository. Only the author can see the report.

Please include:
- the KrogosLab version (and module version, if a module is involved) and your Windows version;
- what the problem is and what an attacker could do with it;
- steps to reproduce or a proof of concept.

What to expect:
- a first reply within **7 days**;
- if the problem is confirmed — a fix in the next release, as soon as possible depending on severity;
- credit in the release notes, if you wish.

## Scope
In scope: the KrogosLab program, its official modules and themes, the installer and the files published in this repository's releases.

How KrogosLab is built, to help you judge the impact:
- the editor and overlays are served by a local web server that listens **only on 127.0.0.1** (by default port 4777) — it is not reachable from other computers;
- API keys (Twitch, YouTube, Groq) are stored only on your PC in `%APPDATA%\KrogosLab` and are never sent to the browser;
- modules from *Settings → Modules* are downloaded from this repository's releases and checked by **SHA-256** before installation;
- you can check every download against `KrogosLab-<version>-SHA256.txt` in the release.

Out of scope:
- builds, modules or themes not published in this repository;
- problems of third-party services (Twitch, YouTube, Groq, Spotify, OBS, model hosting sites);
- attacks that already require administrator rights or full control of the PC;
- the Windows SmartScreen warning: the program is not yet signed with a paid certificate (see the [FAQ](https://github.com/TiDaGo/KrogoshLab/wiki/FAQ)).

RU <img src="https://flagcdn.com/20x15/ru.png" width="20" height="15" alt="RU">
## Поддерживаемые версии
Исправления безопасности выходят только для **последней версии** KrogosLab и её модулей. Прежде чем сообщать о проблеме, обновитесь: [последний релиз](../../releases/latest).

## Как сообщить об уязвимости
Пожалуйста, **не открывайте** публичный issue о проблеме безопасности.
Сообщите о ней закрыто: **[Security → Report a vulnerability](../../security/advisories/new)** в этом репозитории. Сообщение видит только автор.

Укажите:
- версию KrogosLab (и версию модуля, если дело в модуле) и версию Windows;
- в чём проблема и что с её помощью может сделать злоумышленник;
- шаги воспроизведения или пример (proof of concept).

Чего ожидать:
- первый ответ — в течение **7 дней**;
- если проблема подтвердится — исправление в ближайшем релизе, как можно скорее в зависимости от опасности;
- упоминание в описании релиза, если вы хотите.

## Что входит
Входит: программа KrogosLab, её официальные модули и темы, установщик и файлы, опубликованные в релизах этого репозитория.

Как устроен KrogosLab — чтобы проще оценить последствия:
- редактор и оверлеи отдаёт локальный веб-сервер, который слушает **только 127.0.0.1** (по умолчанию порт 4777) — с других компьютеров он недоступен;
- ключи API (Twitch, YouTube, Groq) хранятся только на вашем ПК в `%APPDATA%\KrogosLab` и никогда не передаются в браузер;
- модули из «Настройки → Модули» скачиваются из релизов этого репозитория и перед установкой проверяются по **SHA-256**;
- любую загрузку можно сверить с `KrogosLab-<версия>-SHA256.txt` в релизе.

Не входит:
- сборки, модули и темы, опубликованные не в этом репозитории;
- проблемы сторонних сервисов (Twitch, YouTube, Groq, Spotify, OBS, сайтов с моделями);
- атаки, для которых уже нужны права администратора или полный контроль над ПК;
- предупреждение Windows SmartScreen: программа пока не подписана платным сертификатом (см. [FAQ](https://github.com/TiDaGo/KrogoshLab/wiki/FAQ)).
