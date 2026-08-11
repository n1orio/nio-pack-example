# NIO Pack Example

Сборка-пример для [NIO Launcher](https://github.com/n1orio/nio-launcher): демонстрирует **все возможности лаунчера, кроме платной сборки** (Boosty).

## Что здесь показано

| Файл | Возможность |
| --- | --- |
| `servers.json` | Авторские сервера во вкладке «Сервера» (порт и описание) |
| `socials.json` | Ссылки на соцсети автора в шапке сборки |
| `theme.json` | Зелёная тема лаунчера под стиль сборки |
| `pack.json` → `minRam: 4096` | Минимальная оперативка: бейдж «≥ 4 ГБ» и защита от запуска при нехватке ОЗУ |
| релизы с `.mrpack` | Новости: релизы сборки появляются в ленте |
| GitHub Releases | Автообновления и выбор версии |

Платная сборка (подписка Boosty) намеренно **не** показана: для неё нужно указать `boostyBlog` в `pack.json`.

## Ссылка-приглашение

Одна универсальная ссылка для всех игроков (работает для любой сборки, подставьте свой адрес вместо примера):

```
https://n1orio.github.io/nio-launcher/?url=https%3A%2F%2Fgithub.com%2Fn1orio%2Fnio-pack-example&name=Example%20Pack
```

- у кого установлен NIO Launcher — он откроется и добавит сборку автоматически;
- у кого нет — страница предложит скачать лаунчер.

Такую ссылку можно вставлять в README, описания релизов и Discord.

## Как подключить

В лаунчере: вкладка «Разработчикам» → «Добавить сборку» → вставьте ссылку на этот репозиторий:

```
https://github.com/n1orio/nio-pack-example
```

или на файл:

```
https://github.com/n1orio/nio-pack-example/releases/latest/download/example-pack.mrpack
```

## Формат

Каждый релиз репозитория должен содержать два файла:

| Файл | Описание |
| --- | --- |
| `*.mrpack` | Модпак в формате Modrinth Pack (экспорт из Prism Launcher) |
| `pack.json` | Описание сборки (см. ниже) |

### pack.json

```json
{
  "name": "Example Pack",
  "id": "example-pack",
  "version": "1.1.0",
  "description": "Сборка-пример для NIO Launcher: демонстрация всех возможностей",
  "author": "NIO",
  "minRam": 4096
}
```

Обязательные поля: `name`, `version`. Необязательные:

- `minRam` — минимальная оперативка для запуска в МБ (4096 = 4 ГБ): лаунчер покажет
  бейдж у сборки и не даст запустить игру при меньшем выделении ОЗУ.
- `boostyBlog` — ник блога на Boosty: делает сборку **платной** (скачивание и запуск
  только для подписчиков блога). Без него сборка бесплатная.

### servers.json (необязательно)

Сервера автора во вкладке «Сервера» (статус онлайн/игроки, «Играть на сервере»):

```json
[
  { "name": "Example Survival", "ip": "play.example.com", "desc": "Выживание" },
  { "name": "Example SkyBlock", "ip": "sky.example.com", "port": 25570, "desc": "Свой порт" }
]
```

### socials.json (необязательно)

Ссылки на соцсети в шапке сборки (только `https://`, до 8 ссылок):

```json
{
  "discord": "https://discord.gg/example",
  "telegram": "https://t.me/example",
  "youtube": "https://youtube.com/@example"
}
```

### theme.json (необязательно)

Тема лаунчера под стиль сборки (hex-цвета, лаунчер плавно перекрасится при открытии):

```json
{
  "bg": "#0a140d",
  "panel": "#10241a",
  "input": "#16301f",
  "border": "#1f4030",
  "tx": "#d7ebe0",
  "txStrong": "#f0faf5",
  "txMuted": "#8fb8a4",
  "accent": "#4ade80",
  "accentStrong": "#86efac",
  "accentHover": "#22c55e",
  "accentDeep": "#16a34a"
}
```

## Как собрать свой модпак

1. Prism Launcher: File → Export Instance → **Modrinth pack (.mrpack)**.
2. Положите файл `.mrpack` и `pack.json` в релиз GitHub (Releases → Create a new release).
3. Вставьте ссылку на репозиторий в лаунчер — всё.
