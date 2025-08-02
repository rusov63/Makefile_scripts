# Makefile aiogram - Структура для Телеграм бота

# Параметры для виртуального окружения
VENV_NAME=.venv
PYTHON=python3.12
PIP=$(VENV_NAME)/bin/pip

# Параметры для создание структуры проекта
MKDIR=bot

#DJANGO_MANAGE=$(VENV_NAME)/bin/python manage.py

# Цели
.PHONY: all install structure fill_file

all: install structure fill_file

install:
	@echo "Создание виртуального окружения и установка зависимостей..."

	$(PYTHON) -m venv $(VENV_NAME)
	source $(VENV_NAME)/bin/activate && \
	$(PYTHON) -m pip install --upgrade pip && \
	$(PIP) install -r requirements.txt
	$(PIP) freeze > requirements.txt


structure:
	@echo "Создаем структуру проекта..."

	touch run.py bot_start.py config.py readme.md
	touch .env env.sample .gitignore

	mkdir -p $(MKDIR)/handlers $(MKDIR)/keyboards $(MKDIR)/database $(MKDIR)/tests \
	$(MKDIR)/other_files && \
	touch $(MKDIR)/__init__.py && \
	touch $(MKDIR)/other_files/echo.py $(MKDIR)/other_files/feedback_project.py
	mkdir -p media/image && mkdir -p media/documents

	@echo "Все создано. Ошибок нет"

fill_file:
	@echo "Заполняем файл .gitignore, readme.md"

	@curl -o .gitignore https://raw.githubusercontent.com/rusov63/.gitignore/main/.gitignore
	@echo "Почти все..."
	@curl -o readme.md https://raw.githubusercontent.com/rusov63/.gitignore/main/add_readme.md

	@echo "Файлы заполнены. Ошибок нет"
#run:
#	@echo "Запуск сервера разработки Django..."
#	$(DJANGO_MANAGE) runserver
#
#migrate:
#	@echo "Применение миграций..."
#	$(DJANGO_MANAGE) migrate
#
#makemigrations:
#	@echo "Создание миграций..."
#	$(DJANGO_MANAGE) makemigrations
#
#shell:
#	@echo "Запуск оболочки Django..."
#	$(DJANGO_MANAGE) shell

#clean:
#	@echo "Удаление виртуального окружения..."
#	rm -rf $(VENV_NAME)

