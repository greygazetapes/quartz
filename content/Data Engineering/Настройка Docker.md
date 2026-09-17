**1. Настройка в Docker Desktop**

Устанавливаем Docker Desktop. Авторизуемся.

Заходим в Settings -> Resources -> WSL integration.

Ставим галочку, добавляя доступ для WSL:

	Configure which WSL 2 distros you want to access Docker from.
	
	Enable integration with my default WSL distro

Применяем настройки.

**2. Настройка в WSL**

Мы применили Docker для WSL, после этого должен быть доступен просмотр версии Docker непосредственно в WSL - `docker --version`.

Используется группа пользователей `docker` для того, чтобы иметь возможность управления контейнерами и запрашивать доступ к демону Docker без прав суперпользователя (`sudo`).

Добавляем пользователя в группу `docker` при помощи команды: `sudo usermod -aG docker $USER`.

После успешного добавления необходимо обновить группу пользователей `docker` при помощи команды: `newgrp docker`.

**3. Сборка инфраструктуры Docker**

После этого собираем инфраструктуру докера командой: `docker compose up -d`.

Просматриваем при помощи команды: `docker compose ps`.

