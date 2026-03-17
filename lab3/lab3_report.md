Что сделано

- Создан репозиторий для лабораторной работы lab3 и склонирован на локальный компьютер
- Создана папка prometheus с конфигурацией Prometheus
<img width="1319" height="723" alt="image" src="https://github.com/user-attachments/assets/61e0f035-628a-4fdc-876a-ba525dba54bb" />

- Создан файл prometheus/prometheus.yml с настройкой scrape для Prometheus и node-exporter
<img width="1319" height="723" alt="image" src="https://github.com/user-attachments/assets/f38ab18a-c053-4956-ac7c-5084bc40bbc9" />
- Создана сеть monitoring для совместной работы контейнеров
- Создан том prometheus-data для хранения данных Prometheus
- Запущен контейнер Node Exporter для сбора системных метрик
<img width="1319" height="723" alt="image" src="https://github.com/user-attachments/assets/263f65a6-c562-4360-9589-28054be52ca1" />
- Проверена работа Node Exporter через curl http://localhost:9100/metrics, метрики собираются
<img width="1319" height="723" alt="image" src="https://github.com/user-attachments/assets/c9a9c909-0d33-4cab-9991-0b1767343178" />
<img width="1319" height="723" alt="image" src="https://github.com/user-attachments/assets/48a007b2-64e8-4858-b0b2-d8e784745e6d" />
- Запущен контейнер Prometheus с подключением к сети monitoring и монтированием папки с конфигурацией и тома данных
- Проверена работа Prometheus через браузер на http://localhost:9090
<img width="1319" height="723" alt="image" src="https://github.com/user-attachments/assets/4e962314-6f70-4b67-9bb8-971e358fadc3" />
<img width="1424" height="561" alt="image" src="https://github.com/user-attachments/assets/d462c010-781d-4ce6-bc50-de3e6e7b1b84" />
- Создан том grafana-data для хранения данных Grafana
- Запущен контейнер Grafana с подключением к сети monitoring, проверена работа на http://localhost:3000 (логин admin, пароль admin)
<img width="1322" height="561" alt="image" src="https://github.com/user-attachments/assets/4809fc06-044e-45a2-85c8-a5d4ffc7f500" />
- В Grafana добавлен источник данных Prometheus с URL http://prometheus:9090
<img width="1322" height="743" alt="image" src="https://github.com/user-attachments/assets/9b3309a3-e6df-4ec6-be8f-a10b325fee67" />
- Создан дашборд Grafana с отдельными панелями для метрик CPU и диска
- Проверено отображение метрик в Grafana, графики обновляются в реальном времени
<img width="1322" height="724" alt="image" src="https://github.com/user-attachments/assets/355b7b00-6307-4ca6-93af-57fda8373460" />
