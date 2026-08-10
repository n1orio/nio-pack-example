# NIO Pack Example

Минимальный пример сборки для [NIO Launcher](https://github.com/n1orio/nio-launcher).

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
  "version": "1.0.0",
  "description": "Минимальная сборка-пример для NIO Launcher"
}
```

Обязательные поля: `name`, `version`. Значение `name` используется лаунчером как название сборки.

## Как собрать свой модпак

1. Prism Launcher: File → Export Instance → **Modrinth pack (.mrpack)**.
2. Положите файл `.mrpack` и `pack.json` в релиз GitHub (Releases → Create a new release).
3. Вставьте ссылку на репозиторий в лаунчер — всё.
