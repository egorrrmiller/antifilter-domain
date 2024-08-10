# Назначение

Cборки dat-файлов для проектов V2Fly, XRay и подобных на основе списков пользователя [ItDog](https://github.com/itdoginfo/allow-domains)
Сборка проводится автоматически, ежедневно в 8 часов через GitHub Actions.

# Использованные списки
- Файл ```domains.dat``` собирается на основе списка <https://raw.githubusercontent.com/itdoginfo/allow-domains/main/Russia/inside-raw.lst>

# Ссылки на скачивание

- **domains.dat**：<https://github.com/egorrrmiller/antifilter-domain/releases/latest/download/domains.dat>
- wget -O /usr/share/xray/domains.dat <https://github.com/egorrrmiller/antifilter-domain/releases/latest/download/domains.dat>

# Пример использования

## v2rayA
![image](https://github.com/user-attachments/assets/955e8dde-9d7a-44e3-a0b6-d3f8e5d82a2f)

## XRay and etc.
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
