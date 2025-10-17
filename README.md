# Zadania powtórkowe: Przetwarzanie plików tekstowych

## Zadanie 4

W wybranej technologii (**Python, Java, C++, PHP, Node.js**) zaimplementuj skrypt/program sieciowy **CRASHXL** do pobierania zasobów, podobny w działaniu do programu `wget` lub `curl`.

### Wytyczne

- Program będzie posiadał plik konfiguracyjny (`C`) na informacje oznaczone dużymi literami alfabetu.
- Pobierze z lokalizacji zdalnej (`R`) lub w przypadku braku Internetu z lokalizacji alternatywnej (`A`) plik tekstowy (`S`) zawierający listę innych plików do pobrania.
- Pliki z w/w listy (`S`) (prosty plik tekstowy – jedna nazwa pliku w jednej linii) zapisze do wskazanego katalogu (`H`).
- Obsłuży błędy pobierania (brak pliku do pobrania w zdalnej lokalizacji `R`, długi czas oczekiwania, błąd uprawnień lub zapisu na dysku).
- Sprawdzi, czy kopia pliku tego skryptu/programu (`S`) znajduje się w katalogu `X` oraz jaką ma wersję.
- Jeżeli katalogu nie ma, to go utworzy, jeżeli pliku nie ma to go wgra, jak jest to porówna wersję i w razie potrzeby nadgra nowszą.
- Zapisze podejmowane akcje w pliku dziennika (`L`) z datą i godziną w formacie:

```
RRRR-MM-DD hh:mm:ss AKCJA
```

- Program pozwoli na tworzenie nowego pliku konfiguracyjnego przyjmując informacje w formie interaktywnej lub jako seria parametrów dostarczanych podczas uruchamiania programu.

---

### Przykład pliku konfiguracyjnego

```
C = ~/.config/crashxl/conf.ext
R = https://edu.gplweb.pl/sh/
A = 10.4.0.117/sh/
S = scripts.lst
H = ~/Pobrane/
X = /opt/crashxl
L = /var/log/crashxl
```

> Ścieżki do plików i katalogów muszą być tłumaczone do używanego systemu operacyjnego, czyli np. dyrektywa `~/Pobrane` dla Linuksa oznacza `/home/USER/Pobrane`, a dla Windows `C:\Users\USER\Pobrane`. Informację o adresie IP (`A`) dopasuj do adresu IP swojej stacji roboczej.

---

### Przykład listy plików (`S`)

```
file=1.txt
file=2.txt
file=3.txt
```

> Plik `3.txt` NIE istnieje celowo.

---

Testowanie i Dokumentowanie  
Grzegorz Petri / 2024
