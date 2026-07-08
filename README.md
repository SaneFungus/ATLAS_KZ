# Atlas Zakazanych Książek — Przestrzeń Projektowa

Ten katalog zawiera pliki bazowe dla interaktywnego projektu **Atlas Zakazanych Książek**, zaimplementowanego jako statyczna aplikacja internetowa (Single Page Application) przystosowana pod darmowy hosting **GitHub Pages**.

## 🛠️ Zawartość Struktury:
1. `index.html` - Warstwa wizualna (Frontend) wykonana przy użyciu czystego JavaScriptu i Tailwind CSS CDN. Zawiera dynamiczne moduły sortowania, wyszukiwania, system filtrów po archetypach oraz pełny, responsywny widok szczegółowy karty lektury. Posiada wbudowany mechanizm fallback, zapobiegający awarii aplikacji w trybie bezserwerowym (CORS file:// protocol).
2. `books.json` - Relacyjna struktura bazy danych (Backend/Core) zawierająca ustrukturyzowane wpisy kart książek z podziałem na 9 sekcji merytorycznych oraz tablice liczbowe ocen wpływu.

## 🚀 Instrukcja Wdrożenia na GitHub Pages:
1. Utwórz nowe, publiczne repozytorium na swoim koncie GitHub (np. o nazwie `atlas-zakazanych-ksiazek`).
2. Wgraj bezpośrednio do gałęzi głównej (`main` lub `master`) dwa wygenerowane pliki: `index.html` oraz `books.json`.
3. Przejdź do ustawień repozytorium: **Settings** -> **Pages**.
4. W sekcji **Build and deployment** ustaw źródło (*Source*) na **Deploy from a branch**, wybierz gałąź `main` / `/ (root)` i kliknij **Save**.
5. Po upływie 1-2 minut Twoja aplikacja będzie dostępna publicznie pod unikalnym adresem URL udostępnianym przez GitHub.

## 🤖 Workflow Współpracy z LLM (Gemini):
Podczas generowania kolejnych partii książek z dowolnego z 7 archetypów cenzury, poproś model o podawanie danych w ustrukturyzowanym formacie JSON zgodnym ze schematem z pliku `books.json`. Po wygenerowaniu kodu przez model wystarczy dokleić elementy na koniec tablicy w pliku `books.json`, a system automatycznie przebuduje interfejs, zaktualizuje liczniki oraz filtry na stronie głównej przy kolejnym uruchomieniu.
