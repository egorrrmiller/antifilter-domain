# Назначение

Форк оригинального проекта для сборки dat-файлов Geosite для проектов V2Fly, XRay и подобных на основе списков [Antifilter](https://github.com/itdoginfo/allow-domains)
Сборка проводится автоматически еженедельно через GitHub Actions

## Использованные списки
- Файл ```domains.dat``` собирается на основе списка <https://raw.githubusercontent.com/itdoginfo/allow-domains/main/Russia/inside-raw.lst>

## Ссылки на скачивание

- **domains.dat**：<https://github.com/egorrrmiller/antifilter-domain/releases/latest/download/domains.dat>

## Пример использования

```json
{
  "routing": {
      "rules": [
      {
        "domain": [
          "ext:domains.dat:antifilter-community"
        ],
        "type": "field",
        "outboundTag": "proxy"
      },
      {
        "type": "field",
        "outboundTag": "direct"
      }
    ]
  }
}
```
