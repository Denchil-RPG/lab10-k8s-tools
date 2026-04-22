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

## Запуск:

```bash
# Helm
helm install promgra ./helm-chart/ --set EXTERNAL_PORT=3456 --set EXTERNAL_IP=10.0.2.15 --set GF_ADMIN_PASSWORD=admin123

# Kustomize
kubectl apply -k kustomize-flask/dev/
cat > ~/lab10_k8s_tools/README.md << 'EOF'
# Лабораторная работа №10: Helm, Kompose, Kustomize

## Студент: Прокопович Д.А. группа Бас-21

## Выполненные задачи:

### 1. Helm + Kompose (prometheus-grafana)
- Конвертирован docker-compose в Helm чарт: `kompose convert -c`
- Создан чарт `promgra` с шаблонами
- Развернут релиз в minikube

### 2. Kustomize (flask-redis)
- Создана базовая конфигурация в `base/`
- Созданы overlay для `dev` и `prod` окружений
- Разные порты: dev - 54321, prod - 12345

## Запуск:

```bash
# Helm
helm install promgra ./helm-chart/ --set EXTERNAL_PORT=3456 --set EXTERNAL_IP=10.0.2.15 --set GF_ADMIN_PASSWORD=admin123

# Kustomize
kubectl apply -k kustomize-flask/dev/

