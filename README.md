# ML_finanse_new

Kolejność odczytu:
* `Prepared_data_and_initial_model_Glazer.ipynb`- wstępna analiza oraz przygotowanie danych (w połowie notebooka zmieniana jest koncepcja, do momentu "Dalsze modelowanie danych") 
* `Initial_model_Adrian.ipynb` - na podstawie pierwszego zbiodu danych `data.csv` powstał model initial
* `Advanced_model_Kwasnioch.ipynb`- na podstawie pierwszego zbiodu danych data.csv powstał model Advanced
* `Prepared_data_and_initial_model_Glazer.ipynb` - (od momentu"Dalsze modelowanie danych") dodanie nowych zmiennych oraz wyuczenie nowego initial modelu, na podstawie zbioru danych `data_with_indicators.csv`

# Wymagania funkcjonalne

## Eksploracja i przygotowanie danych 
- Odczytuje dane wejściowe otrzymane na zajęciach, które opisują: Date, Tiker, Kategorię firmy oraz wyliczoną wartość
- Dostarcza wizualizacje odczytanych danych, głównie w postaci tabelarycznej, które informują o podstawowych rozkładach i cechach danych
- Oczyszcza dane: zmienia typ wczytanych danych (format), usuwa bezużyteczne dane, usuwa niepotrzebne kolumny
- Generuje nowe cechy poprzez przekształcanie danych obecnych w zbiorze (tworzenie Y).
- Pobiera dane o cenach akcji i dołącza do zbioru danych (również na okres poprzedzający ostatnią date dla danego Tickera)
- Wzbogaca zbiór o wskaźniki finansowe za pomocą biblioteki "ta"
, pomijając wskaźniki odpowiedzialne za obliczenie stopy zwrotu (naszego Y) 
- Zapisuje ostateczny zbiór danych do pliku, który będzie wykorzystywany w dalszych krokach.

## Modelowanie wstępne - regresja liniowa
- Importuje odpowiednie biblioteki potrzebne do analizy
- Otwiera przygotowany wcześniej zbiór danych
- Przekształca zbiór na zmienne objaśniane oraz objaśniające 
- Wybiera ostateczny zestaw należytych cech 
- Wykonuje podział train test 
- Trenuje model liniowy oraz sprawdza jego poprawność
- Zapisuje otrzymany model 
- Przeprowadza 5-krotny test walidacji krzyżowej oraz sprawdza poprawność modelu dla każdej z walidacji

## Zaawansowane modelowanie
- Import bibliotek
- Wczytanie zbioru danych
- Podział zbioru na testowy, walidacyjny oraz treningowy (biblioteką fast_ml lub sklearn)
- Wczytanie wymienionych modeli: XGBoost, Random Forest, LSTM oraz GRU (za pomocą PyTorch)
- W dwóch pierwszych modelach ustawienie parametrów wejściowych w postaci słownika
- Hiperparametryzacja za pomocą GridSearch
- trening modelu
- ocena metryk
- walidacja krzyżowa za pomocą KFolds lub Stratified KFolds
- Zapis najlepszego modelu






