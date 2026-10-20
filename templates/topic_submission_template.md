# Zgłoszenie tematu

Odpowiedź mieści się na jednej stronie. Projekt dotyczy nadzorowanej klasyfikacji jednolabelowej: każdy przykład ma dokładnie jedną klasę.

1. Roboczy tytuł: Klasyfikacja chorób siatkówki oka na podstawie zdjęć dna oka z uwzględnieniem pacjenta jako jednostki generalizacji.
2. Modalność (tekst, obraz, audio albo dane multimodalne): Obraz
3. Problem klasyfikacji (co jest klasą i ile jest klas): Nadzorowana klasyfikacja jednolabelowa. Klasą jest diagnoza stanu oka; są 4 klasy docelowe (zdrowe oko, retinopatia cukrzycowa, jaskra, zaćma)
4. Pytanie eksperymentalne (co chcesz sprawdzić): Czy wykorzystanie transfer learningu z zamrożonym bądź częściowo dostrojonym enkoderem ConvNeXt/ResNet-50 pozwoli osiągnąć istotnie wyższy wynik F1-macro w porównaniu do klasycznego baseline opartego na cechach kolorystyczno-teksturowych (histogramy RGB + cechy GLCM) i klasyfikatorze Random Forest, przy zachowaniu podziału pacjentów wykluczającego wyciek danych?
5. Źródło danych (link): https://www.kaggle.com/datasets/andrewmvd/ocular-disease-recognition-odir5k
6. Przybliżona wielkość zbioru: Około 3 500 – 4 000 wyselekcjonowanych obrazów
7. Lista klas i sposób oznaczenia etykiet:
  0: Normal (brak zmian chorobowych)
	1: Diabetes (retinopatia cukrzycowa)
	2: Glaucoma (jaskra)
	3: Cataract (zaćma)
8. Licencja danych: CC BY-NC-SA 4.0 (użytek niekomercyjny, naukowy i dydaktyczny)
9. Proponowana jednostka generalizacji: Pacjent (Patient ID)
10. Planowany baseline: Ekstrakcja ręcznie projektowanych cech obrazu (statystyki kanałów kolorów RGB/HSV oraz cechy tekstury GLCM) z klasyfikatorem Random Forest (scikit-learn)
11. Wstępny pomysł na model pretrained: Model convnext_tiny lub resnet50 wstępnie wytrenowany na zbiorze ImageNet (pobrany z timm / torchvision)
12. Potencjalne ograniczenia obliczeniowe: Przeskalowanie obrazów do stałego rozmiaru (np. 224x224 px) ze względu na ograniczenia VRAM GPU. Trening na darmowym GPU (Google Colab / Kaggle) z małym rozmiarem batcha (batch size = 16 lub 32)
13. Dane osobowe, wrażliwe albo z ograniczeniami dostępu lub redystrybucji (tak albo nie; jeśli tak, jak je przechowasz): Nie
