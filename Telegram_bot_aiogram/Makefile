# Шаблон проекта Telegram-бота на aiogram.

# Параметры для виртуального окружения
VENV_NAME=.venv
PYTHON=python3.12
PIP=$(VENV_NAME)/bin/pip

# Параметр названия директории проекта
MKDIR=bot


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

	touch $(MKDIR)/handlers/__init__.py
	touch $(MKDIR)/keyboards/__init__.py
	touch $(MKDIR)/database/__init__.py
	touch $(MKDIR)/tests/__init__.py
	touch $(MKDIR)/other_files/__init__.py

	@echo "Все создано. Ошибок нет"

fill_file:
	@echo "Заполняем файл .gitignore, readme.md"
	@echo "BOT_TOKEN=your_token_here" > .env
	@echo "BOT_TOKEN=your_token_here" > env.sample
	@curl -o .gitignore https://raw.githubusercontent.com/rusov63/.gitignore/main/.gitignore
	@echo "Почти все..."
	@curl -o readme.md https://raw.githubusercontent.com/rusov63/.gitignore/main/add_readme.md

	@echo "Файлы заполнены. Ошибок нет"

	@echo "import os\nfrom dotenv import load_dotenv\n\nload_dotenv()\n\nclass Config:\n    def __init__(self):\n        self.bot_token = os.getenv('BOT_TOKEN')\n        self.admin_id = os.getenv('ADMIN_ID')\n" > config.py
