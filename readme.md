# Конструктор шаблонов проектов 🛠️

![Make](https://img.shields.io/badge/Make-%23FFD7B5.svg?logo=cmake&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white)
![Aiogram](https://img.shields.io/badge/Aiogram-2CA5E0?logo=telegram&logoColor=white)

## 📌 Описание

Универсальный инструмент для быстрого развертывания проектных шаблонов с использованием Makefile. Поддерживает:

✔ Создание виртуального окружения (venv)  
✔ Установку зависимостей через pip  
✔ Генерацию структуры проекта  
✔ Автозаполнение конфигурационных файлов (.gitignore, .env, README.md)  

## 🛠 Основные возможности

- **Готовые шаблоны**:
  - `Telegram_bot_aiogram/` - полный каркас для бота на Aiogram 3.x
  - `Web_project_django/` - стартовый шаблон Django-проекта

## 🔧 Требования

```bash
make --version || sudo apt install make  # Для Ubuntu/Debian
```

## 🚀 Быстрый старт

1. Клонируйте репозиторий:
```bash
git clone https://github.com/rusov63/Makefile_scripts
cd Makefile_scripts
```

2. Выберите проект, перейдите в него. Инициализируйте проект:
```bash
make
```
Команда вызовет цель all которая последовательно выполняет цели install, structure и fill_file.

> **Важно**: Убедитесь, что в каталоге присутствуют:
> - `Makefile`
> - `requirements.txt` с актуальными зависимостями

## 📂 Структура шаблонов

```
Makefile_scripts/
├── Telegram_bot_aiogram/
│   ├── Makefile
│   └── requirements.txt
├── Web_project_django/
│   ├── Makefile
│   └── requirements.txt
└── README.md
```

## 🗑️ Удаление ненужных проектов
После создания проекта удалите шаблоны, которые вам не потребуются.

## 📬 Контакты
Если у вас есть вопросы или предложения, пожалуйста, свяжитесь со мной:  
📧 rusov63@yahoo.com  
💬 [Telegram](https://t.me/your_username)
