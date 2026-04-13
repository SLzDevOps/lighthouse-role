# Lighthouse Role

Роль для установки и настройки Lighthouse - инструмента для аудита производительности веб-страниц.

## Требования

- ОС: Ubuntu/Debian
- Ansible 2.9+

## Параметры

| Параметр | Описание | Значение по умолчанию |
|----------|----------|----------------------|
| `lighthouse_port` | Порт для веб-сервера Nginx | `80` |
| `lighthouse_server_name` | Имя сервера (server_name) | `localhost` |
| `lighthouse_repo` | Git репозиторий Lighthouse | `https://github.com/VKCOM/lighthouse.git` |
| `lighthouse_version` | Версия/ветка для клонирования | `master` |

## Пример использования

```yaml
- hosts: servers
  roles:
    - role: lighthouse-role
      lighthouse_port: 8080
      lighthouse_server_name: example.com
