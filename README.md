# 🌟 Pollination Flow Manager  


Простой и удобный менеджер для работы с платформой Pollination на JavaScript/Node.js

**🚀 Multi-Repo Project** - Автоматически деплоится на 20 GitHub репозиториев!  

> 📦 Версия 1.1.0 - Улучшенная стабильность

## Установка


```bash
npm install
```

## Быстрый старт

1. Создайте файл `.env` с вашими настройками
2. Запустите `npm start`
3. Готово!

## Использование

```javascript
import { PollinationClient } from './src/client.js';

const client = new PollinationClient();

// Получить проекты
const projects = await client.getProjects();

// Создать проект
const newProject = await client.createProject({
    name: 'My Project',
    description: 'Описание проекта'
});

// Отправить задачу
const job = await client.submitJob(projectId, {
    recipe_id: 'recipe-id',
    inputs: { param1: 'value1' }
});
```

## Конфигурация

Создайте файл `.env` с вашими настройками:

```
POLLINATION_API_KEY=your_api_key_here
POLLINATION_BASE_URL=https://api.pollination.cloud
```

## Запуск примеров

```bash
# Базовый пример
node examples/basic-usage.js

# Запуск основного приложения
npm start
```

## Структура проекта

```
pollination-flow-manager/
├── src/
│   ├── index.js      # Главный файл
│   ├── client.js     # API клиент
│   └── models.js     # Модели данных
├── examples/
│   └── basic-usage.js # Примеры использования
├── scripts/
│   └── deploy.js     # Скрипты деплоя
└── package.json
```

## Деплой на GitHub

Смотрите файл `DEPLOY.md` для инструкций по загрузке на несколько GitHub аккаунтов.
Токены находятся в файле `TOKENS.txt`.

## Лицензия

MIT License - свободное использование