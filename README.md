# ML Labs — учебные ноутбуки по машинному обучению

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white)

Коллекция лабораторных работ по классическому ML, нейросетям, компьютерному зрению, обучению без учителя, временным рядам и аудио. Репозиторий оформлен как **пет-проект для портфолио**: каждая тема в отдельной папке с собственным описанием, воспроизводимыми данными там, где они не скачиваются автоматически, и аккуратным `.gitignore` для кэшей и виртуальных окружений.

## Что внутри

| № | Раздел | Кратко о содержании | Документация |
|---|--------|---------------------|--------------|
| 2 | [Линейные модели](02-linears/README.md) | Регрессия, регуляризация, градиентный спуск на табличных данных о соцсетях | [→](02-linears/README.md) |
| 3 | [Нейросеть «с нуля»](03-deep-learning/README.md) | Собственные `Parameter`, оптимизатор (Adam), обучение на `data.csv` и датасете Digits | [→](03-deep-learning/README.md) |
| 4 | [CNN и transfer learning](04-cnn/README.md) | PyTorch, MNIST / Fashion-MNIST, общие веса и дообучение | [→](04-cnn/README.md) |
| 5 | [Обучение без учителя](05-unsupervised/README.md) | Отбор признаков, кластеризация, PCA / t-SNE, SMS spam | [→](05-unsupervised/README.md) |
| 6 | [Временные ряды](06-time-series/README.md) | Анализ и прогноз ряда авиаперевозок (`AirPassengers`) | [→](06-time-series/README.md) |
| 7 | [Аудио и Hugging Face](07-audio/README.md) | Загрузка аудиодатасета, предобработка, классификация | [→](07-audio/README.md) |

## Быстрый старт

```bash
git clone <url-вашего-репозитория>.git
cd ML-labs
python -m venv .venv
.venv\Scripts\activate          # Windows
# source .venv/bin/activate     # Linux / macOS
pip install -r requirements.txt
python -m ipykernel install --user --name=ml-labs --display-name="ML Labs"
jupyter lab
```

Откройте нужный `.ipynb` в подпапке; **данные** лежат рядом с ноутбуком там, где это требуется (см. README внутри раздела).

## Структура репозитория

```
ML-labs/
├── README.md                 ← вы здесь
├── requirements.txt
├── 02-linears/
├── 03-deep-learning/
├── 04-cnn/
├── 05-unsupervised/
├── 06-time-series/
└── 07-audio/
```

## Заметки

- **Лаба 4 (CNN):** датасеты MNIST / Fashion-MNIST подтягиваются из `torchvision` в локальную папку `./data` в каталоге ноутбука (игнорируется в `.gitignore`).
- **Лаба 7:** основной датасет идёт с **Hugging Face**; для части шагов нужен доступ к интернету и при необходимости `huggingface-cli login`.

## Лицензия

Исходные ноутбуки и сопутствующие скрипты в этом репозитории распространяются по лицензии [MIT](LICENSE), если не оговорено иначе. **Данные** из внешних источников (Hugging Face, torchvision и т.д.) остаются под **их** лицензиями — ознакомьтесь с карточкой датасета перед публикацией производных работ.
