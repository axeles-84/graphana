# Изображения

# 📊 Дашборды мониторинга Grafana

Подборка панелей для мониторинга сервера с `node_exporter`:
CPU, память и диски.

---

## 🖥️ Загрузка ядер CPU

Отображение утилизации каждого ядра процессора в процентах.

![Загрузка ядер CPU](https://raw.githubusercontent.com/axeles-84/graphana/main/cores.PNG)

---

## 🔥 Общая загрузка CPU

Сводная панель по всем ядрам: `user`, `system`, `iowait`, `idle`.
Помогает понять, на что именно тратится процессорное время.

![Дашборд CPU](https://raw.githubusercontent.com/axeles-84/graphana/main/cpu.PNG)

---

## 🧠 Использование оперативной памяти

Показывает занятую и доступную память, а также swap.
Ключевая метрика — `MemAvailable`, а не `MemFree`.

![Дашборд памяти](https://raw.githubusercontent.com/axeles-84/graphana/main/memory.PNG)

---

## 💾 Свободное место на дисках

Сводная панель по всем смонтированным файловым системам
(кроме `tmpfs`, `overlay`, `squashfs`).
Помогает увидеть, где заканчивается место.

![Свободное место на дисках](https://raw.githubusercontent.com/axeles-84/graphana/main/freehdd.PNG)

---

## 📦 Использование дискового пространства

Занятое место в процентах и гигабайтах по каждому разделу.
Удобно для быстрой оценки «насколько всё плохо».

![Дашборд HDD](https://raw.githubusercontent.com/axeles-84/graphana/main/hdd.PNG)

---

## 📋 Сводная таблица панелей

| # | Дашборд | Метрика | Файл |
| :-: | :--- | :--- | :--- |
| 1 | Загрузка ядер CPU | `node_cpu_seconds_total` | `cores.PNG` |
| 2 | Общая загрузка CPU | `rate(node_cpu_seconds_total)` | `cpu.PNG` |
| 3 | Использование RAM | `node_memory_MemAvailable_bytes` | `memory.PNG` |
| 4 | Свободное место | `node_filesystem_avail_bytes` | `freehdd.PNG` |
| 5 | Занято на дисках | `node_filesystem_size_bytes` | `hdd.PNG` |


# 📊 PS. 
Дашборды алерты и графики можно настраивать до бесконечности!!! 

