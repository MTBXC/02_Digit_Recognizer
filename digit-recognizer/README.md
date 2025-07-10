# Digit Recognizer - Struktura projektu

## Struktura katalogów

```
digit-recognizer/
│
├── data/                     # Dane wejściowe (symboliczne linki lub pobrane dane)
│   ├── raw/                  # Surowe dane z Kaggle (train.csv, test.csv)
│   └── processed/            # Przetworzone dane (np. znormalizowane, zbalansowane)
│
├── notebooks/               # Notebooki do eksploracji danych i testów
│   └── 01_eda.ipynb         # Eksploracja danych
│   └── 02_baseline.ipynb    # Prosty baseline
│
├── src/                     # Moduły źródłowe projektu
│   ├── config.py            # Konfiguracja (np. ścieżki, hyperparametry)
│   ├── data_loader.py       # Ładowanie i przygotowanie danych
│   ├── features.py          # Feature engineering
│   ├── models/              # Modele i metody treningu
│   │   ├── base_model.py    # Klasa bazowa
│   │   ├── mlp.py           # Przykładowy model MLP
│   │   └── cnn.py           # CNN z PyTorch/Keras
│   ├── utils.py             # Pomocnicze funkcje (seed, logi itp.)
│   └── trainer.py           # Logika treningu, walidacji
│
├── experiments/             # Zapisy eksperymentów
│   ├── logs/                # Logi z treningów (np. TensorBoard, wandb)
│   ├── models/              # Zapisane modele (.pkl/.h5/.pt)
│   └── predictions/         # Pliki submission.csv
│
├── submission/              # Pliki gotowe do submission
│   └── submission_001.csv
│
├── requirements.txt         # Wymagane biblioteki
├── run_experiment.py        # Skrypt do uruchamiania eksperymentów
├── README.md
└── .gitignore
```

## Instrukcja
1. Umieść dane z Kaggle w `data/raw/`.
2. Eksploruj dane i testuj pomysły w `notebooks/`.
3. Rozwijaj kod w `src/`.
4. Wyniki i submission zapisuj w `experiments/` i `submission/`. 