Выбор и настройка мониторинга в системе

Мотивация:
1. Долгая загрузка веб-приложения
2. Множество недостатков при проведении тестирований и долгая публикация приложения на прод
3. Небольшое количество ресурсов команды разработки и тестирования
4. Присутствуют узкие места в системе, что приводит к потере клиентов и негативу со стороны пользователей 

Во избежания проблем с потерей клиентов и негатива пользователей, а также с учетом текущих ограниченных ресурсов команды предлагается внедрить систему мониторинга, что позволит:

1. Улучшить видимость и прослеживаемость системы с точки зрения отказоустойчивости, и в последующем усилить производительность системы
2. Усилить процесс CI\CD и доставки "нужных" обновлений системы 
3. Обнаружить узкие места системы для последующего улучшения производительности системы

Выполнение этих шагов позволит Компании снизить негатив пользователей, привлекать больше клиентов и избежать потери текущих клиентов бизнеса.

Выбор подхода к мониторингу:

1. Подходы USE и RED необходимо использовать для корректного отслеживания использования ресурсов и мониторинга API и Баз данных
2. Четыре золотых сигнала Google для комплексного мониторинга системы

Метрики отслеживания:
1. Для API-сервисов

- CPU и Memory Utilization for shop API, CRM API, MES API- Определение загруженности мощностей сервера ЦПУ и ОЗУ
- Number of responses - количество ответов от приложения
- Unique API Consumers for shop API, CRM API, MES API - количество API пользователей 
- Number of simultanious sessions for shop API, CRM API, MES API - количество одновременных сессий
- Number of HTTP 500 for shop API, CRM API, MES API - выявление ошибок


2. Трафик:

- Kb transferred (received\provided) - объем входящего и исходящего трафика для всех API с целью определение узких мест и резких всплесков повышения нагрузки

3. База данных:

- Memory Utilization для Shop db, MES db
- Number of connections для Shop db, MES db

4. S3 

- KB transfered - отслеживание объема вхходящего\исходящего трафика


План действий:

1. Добавить конфигурацию для Prometheus и развернуть.
2. Добавить необходимые зависимости на всех участках приложений
3. Добавить необходимые метрики для отслеживания в приложениях
4. Развернуть Grafana
5. Настройка Grafana и создание дешбордов для визуализации



