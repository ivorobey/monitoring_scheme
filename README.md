# monitoring_scheme

![image](https://github.com/ivorobey/monitoring_scheme/blob/main/diagram.png)

- Kubernetes: платформа для управления контейнеризированными приложениями и масштабирования их работы. Используется для управления развертыванием всех инструментов в кластере.

- Grafana: инструмент визуализации данных, который используется для создания дашбордов и представления метрик и журналов из Prometheus, Loki и Cortex.

- Prometheus: система мониторинга и оповещения, которая собирает метрики от приложений и инфраструктуры, а затем анализирует их и генерирует оповещения при нарушении заданных правил. Часть метрик может быть отправлена в Cortex.

- Cortex: горизонтально масштабируемая платформа для хранения и запроса метрик, которая использует Minio в качестве хранилища для хранения своих данных. Cortex также может использоваться для агрегирования метрик из нескольких источников.

- Loki: система сбора и хранения журналов, которая использует Minio в качестве хранилища для хранения своих журналов. Loki также может использоваться для поиска и анализа журналов.

- Promtail: агент для отправки журналов в Loki.

- Tempo: система сбора и хранения трассировок, которая использует Minio в качестве хранилища для хранения своих данных. Tempo также может использоваться для поиска и анализа трассировок.

- Minio: объектное хранилище, которое используется для хранения журналов из Loki, данные из Cortex и Tempo.
