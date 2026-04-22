# Лабораторная работа №10: Helm, Kompose, Kustomize

## Студент: Прокопович Д.А. Группа: Бас-21

## Выполненные задачи:

### 1. Helm + Kompose (prometheus-grafana)
- Конвертирован docker-compose в Helm чарт: `kompose convert -c`
- Создан чарт `promgra` с шаблонами
- Развернут релиз в minikube

### 2. Kustomize (flask-redis)
- Создана базовая конфигурация в `base/`
- Созданы overlay для `dev` и `prod` окружений
- Разные порты: dev - 54321, prod - 12345

