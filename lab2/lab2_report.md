University: ITMO University 
Faculty: FICT Course: Введение в веб технологии 
Year: 2025/2026 
Group: U4125 
Author: Vinogradskaia Anastasia Leonidovna 
Lab: Lab2 
Date of create: 17.03.2026 Date of finished: 17.03.2026

1. Подготовка проекта 
- Создана папка lab2 в репозитории и добавлены файлы app.py, requirements.txt, Dockerfile
<img width="341" height="139" alt="image" src="https://github.com/user-attachments/assets/79b1bb68-5442-48bc-ab8e-f7044e19541c" />
- Создан аккаунт на Docker Hub и репозиторий anvinogradskaya/my-flask-app
<img width="1154" height="392" alt="image" src="https://github.com/user-attachments/assets/9a5f72d5-d0ee-4322-9585-768db7c55d54" />


2. Настройка GitHub Actions:
- В корне репозитория создана папка .github/workflows
- Создан файл docker-build.yml с пайплайном
- Настроен запуск пайплайна при пуше в ветку main
- Использован runner ubuntu-latest
- Добавлен шаг checkout для получения кода репозитория
- Настроен Docker Buildx для сборки образа
- Добавлен шаг логина в Docker Hub через secrets
- Настроена сборка и push Docker образа из папки lab2 с тегом anvinogradskaya/my-flask-app:latest
- Добавлен шаг деплоя в виде echo-сообщения
<img width="1154" height="555" alt="image" src="https://github.com/user-attachments/assets/4c44fb3e-d4c5-4b16-831c-d9e389006859" />


3. Настроены секреты в репозитории:
Добавлен DOCKER_USERNAME с логином Docker Hub
Добавлен DOCKER_PASSWORD с паролем
<img width="2360" height="942" alt="image" src="https://github.com/user-attachments/assets/7cbd6705-a963-4861-b850-909d95cc9d22" />
<img width="1154" height="150" alt="image" src="https://github.com/user-attachments/assets/8317d653-a3fa-45e5-bdd4-bd603b7f30e0" />


4. Проведено тестирование:
- Сделан коммит и пуш в ветку main
- Проверено выполнение пайплайна во вкладке Actions
  <img width="1154" height="433" alt="image" src="https://github.com/user-attachments/assets/e3340600-1bec-42a1-b6fd-7d975722d874" />

- Проверены логи каждого шага, подтвержден успешный login, сборка и push образа
<img width="2822" height="1404" alt="image" src="https://github.com/user-attachments/assets/baa2b006-f34f-4360-90f4-4129c740a4dd" />

- проверено появление образа в Docker Hub с тегом latest
<img width="724" height="589" alt="image" src="https://github.com/user-attachments/assets/b6cb6e28-b828-42cb-b157-62c0d949c633" />
