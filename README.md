# Projekt Klasyfikacji Znaków Drogowych z Użyciem Klasyfikatora Bayesa

## Opis Projektu

Ten projekt ma na celu klasyfikację znaków drogowych z wykorzystaniem klasyfikatora Bayesa. Projekt obejmuje przetwarzanie danych, trenowanie modeli klasyfikacyjnych oraz wizualizację wyników.

## Struktura Projektu
project_root/
│
├── data/ # Katalog zawierający dane
│ ├── GTSRB/ # Katalog z danymi GTSRB
│ │ └── Traffic_Signs/ # Przetworzone dane i cechy
│ │ ├── X_train.npy # Obrazy do trenowania
│ │ ├── X_test.npy # Obrazy do testowania
│ │ ├── hu_train.npy # Hu momenty do trenowania
│ │ ├── hu_test.npy # Hu momenty do testowania
│ │ ├── y_train.npy # Etykiety do trenowania
│ │ └── y_test.npy # Etykiety do testowania
│ └── extract_gtsrb.py # Skrypt do rozpakowywania danych
│
├── scripts/ # Katalog zawierający skrypty
│ ├── main.py # Główny skrypt do uruchamiania projektu
│ ├── extract_gtsrb.py # Skrypt do rozpakowywania danych GTSRB
│ ├── preprocess_data.py # Skrypt do przetwarzania danych i obliczania Hu momentów
│ ├── visualize_samples.py # Skrypt do wizualizacji danych
│ ├── train_gaussian_nb.py # Skrypt do trenowania parametrycznego klasyfikatora Bayesa
│ └── train_histogram_nb.py # Skrypt do trenowania nieparametrycznego klasyfikatora Bayesa
│
└── models/ # Katalog do przechowywania wytrenowanych modeli

## Instrukcje do Uruchomienia

### Krok 1: Instalacja Wymaganych Bibliotek

Upewnij się, że masz zainstalowane wszystkie wymagane biblioteki:

```bash
pip install numpy scikit-learn pillow opencv-python matplotlib
```

Projekt Klasyfikacji Znaków Drogowych z Użyciem Klasyfikatora Bayesa
Opis Projektu

Ten projekt ma na celu klasyfikację znaków drogowych z wykorzystaniem klasyfikatora Bayesa. Projekt obejmuje przetwarzanie danych, trenowanie modeli klasyfikacyjnych oraz wizualizację wyników.
Struktura Projektu
Foldery

    data/: Katalog z danymi, zawierający zestaw danych GTSRB.
        GTSRB/: Podkatalog z surowymi danymi GTSRB.
            Traffic_Signs/: Katalog z przetworzonymi danymi i cechami.
                X_train.npy: Plik NumPy zawierający obrazy do trenowania.
                X_test.npy: Plik NumPy zawierający obrazy do testowania.
                hu_train.npy: Plik NumPy zawierający Hu momenty do trenowania.
                hu_test.npy: Plik NumPy zawierający Hu momenty do testowania.
                y_train.npy: Plik NumPy zawierający etykiety do trenowania.
                y_test.npy: Plik NumPy zawierający etykiety do testowania.

    scripts/: Katalog zawierający skrypty pomocnicze do przetwarzania i wizualizacji danych.

Pliki

    main.py: Główny skrypt do uruchamiania wszystkich kroków projektu.
        Opis: Skrypt główny uruchamiający kolejne kroki projektu, od rozpakowywania danych, przez przetwarzanie, po trenowanie modeli i wizualizację wyników.

    extract_gtsrb.py: Skrypt do rozpakowywania danych GTSRB.
        Opis: Skrypt rozpakowujący zestaw danych GTSRB z pliku ZIP do odpowiedniego katalogu.

    preprocess_data.py: Skrypt do przetwarzania danych i obliczania Hu momentów.
        Opis: Skrypt przetwarzający obrazy znaków drogowych, obliczający Hu momenty oraz dzielący dane na zestawy treningowe i testowe.

    visualize_samples.py: Skrypt do wizualizacji danych.
        Opis: Skrypt do wizualizacji przykładowych obrazów i ich Hu momentów z zestawu danych.

    train_gaussian_nb.py: Skrypt do trenowania parametrycznego klasyfikatora Bayesa.
        Opis: Skrypt trenujący parametryczny model klasyfikatora Bayesa (Gaussian Naive Bayes) i generujący raport z wyników klasyfikacji.

    train_histogram_nb.py: Skrypt do trenowania nieparametrycznego klasyfikatora Bayesa.
        Opis: Skrypt trenujący nieparametryczny model klasyfikatora Bayesa (Histogram Bayes) i generujący raport z wyników klasyfikacji.

Instrukcje do Uruchomienia
Krok 1: Instalacja Wymaganych Bibliotek

Upewnij się, że masz zainstalowane wszystkie wymagane biblioteki:

bash

pip install numpy scikit-learn pillow opencv-python matplotlib

Krok 2: Pobranie Zestawu Danych

Pobierz zestaw danych GTSRB i umieść go w katalogu data/GTSRB/ w postaci pliku ZIP o nazwie gtsrb.zip.
Krok 3: Uruchomienie Projektu

Uruchom główny skrypt, który przeprowadzi wszystkie kroki projektu:

bash

python main.py

Szczegółowy Opis Kroków

    Rozpakowywanie danych: Skrypt extract_gtsrb.py rozpakowuje zestaw danych GTSRB do katalogu data/GTSRB/Traffic_Signs/.

    Przetwarzanie danych: Skrypt preprocess_data.py przetwarza obrazy, oblicza Hu momenty i dzieli dane na zestawy treningowe i testowe.

    Wizualizacja danych: Skrypt visualize_samples.py wizualizuje przykładowe obrazy oraz ich Hu momenty.

    Trenowanie modeli: Skrypty train_gaussian_nb.py oraz train_histogram_nb.py trenują odpowiednio parametryczny (Gaussian Naive Bayes) oraz nieparametryczny (Histogram Bayes) klasyfikator Bayesa i generują raporty z wyników klasyfikacji.