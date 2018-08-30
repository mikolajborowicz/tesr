Struktura strony internetowej 

 <!DOCTYPE html>
 <html lang="pl">
 <head>
  <meta charset="utf-8">
  <title>Książki science-fiction, które musisz przeczytać!</title>
  <meta name="description" content="Lista najlepszych książek z zakresu fantastyki, science-fiction wartych przeczytania! Fantastyka naukowa - TOP Lista Wszech Czasów">
  <meta name="keywords" content="książki, science, fiction, fantastyka, sf">
  <meta name="author" content="Trevor Philips Industries">
  <meta http-equiv="X-Ua-Compatible" content="IE=edge,chrome=1">
  <link rel="stylesheet" href="main.css">
  <script src="code.js"></script>
 </head>

 <body>

 </body>
 </html>
Rozpocznijmy analizę od doctype’u:

<!DOCTYPE html>
Informujemy przeglądarkę, iż niniejszy dokument należy potraktować jako zapisany w standardzie HTML 5. Oczywiście przeglądarka posiada wiele mechanizmów kompatybilności wstecznej ze standardami HTML 4.01 i XHTML (więc jeżeli zapiszemy coś wg starszej metody nie będzie wielkiego problemu), niemniej jednak taka deklaracja powinna się znaleźć jako pierwsza w kodzie Twojej strony. Starsze deklaracje były dużo dłuższe, bo zawierały tzw. wpis DTD (ang. document type definition) – przykłady starszych deklaracji znajdziesz na przykład w W3Schools.

To teraz pora sprawić, aby polskie ogonki wyświetlały się poprawnie. Potrzebujemy dopilnować obecności dwóch zapisów oraz poprawnie ustawić kodowanie pliku HTML:

1. Ustawienie polskiego języka witryny:

<html lang="pl">
2. Użycie zestawu znaków utf-8 (lub ewentualnie iso-8859-2) – tag meta charset powinien być pierwszym tagiem wstawionym do sekcji head.

<meta charset="utf-8">
Istnieje także dłuższa wersja tagu, którą można stosować zamiennie z wersją powyższą – więcej szczegółów znajdziesz tutaj.

3. To samo kodowanie (zestaw znaków, czyli charset) ustawiamy dla naszego dokumentu HTML – kodowanie można sprawdzić / zmienić w edytorze (IDE). W przypadku Notepada++ zaglądamy do menu Format (lub w wersji angielskiej interfejsu do opcji Encoding).

To teraz pora określić tytuł (znaczniki title):

<title>Książki science-fiction, które musisz przeczytać!</title>
Tytuł podstrony jest bardzo ważny w kontekście SEO – zwróć szczególną uwagę na jego długość (wykorzystaj całe dostępne miejsce) oraz zawartość (tytuł powinien zawierać kluczowe frazy, na które pozycjonujemy witrynę).

Kolejny ważny w kontekście SEO znacznik meta – opis strony w wyszukiwarce:

<meta name="description" content="Lista najlepszych książek z zakresu fantastyki, science-fiction wartych przeczytania! Fantastyka naukowa - TOP Lista Wszech Czasów">
Do dyspozycji mamy około 155-160 znaków. Opis powinien składać się zarówno z kluczowych fraz, jak również bezpośrednio zwracać się do internauty / zainteresować go właśnie naszą witryną.

Pora na słowa kluczowe (meta keywords):

<meta name="keywords" content="książki, science, fiction, fantastyka, sf">
Co prawda robot Google’a obecnie praktycznie ignoruje tę sekcję (z powodu nadużyć internautów w przeszłości), jednak po dziś dzień umieszczamy ją w kodzie witryny wpisując kilka najbardziej kluczowych, reprezentatywnych dla witryny fraz. Robimy to pomimo traktowania po macoszemu tego znacznika – ot, bez przesadnej czułości i płonnych nadziei wstawiamy go siłą tradycji nie licząc jednak na zbyt wiele benefitów w zamian.

Określenie autorstwa witryny:

<meta name="author" content="Trevor Philips Industries">
Tag opcjonalny, ale wciąż możliwy do umieszczenia. W praktyce dużo lepiej podpisać się na stronie linkiem do własnej witryny (znacznik <a>) – wówczas przynajmniej zyskujemy kolejny link prowadzący do nas w rezultatach wyszukiwania Google (a to już wymierna korzyść). Warto jeszcze zatroszczyć się o poprawne wyświetlenie witryny w starszych wersjach IE:

<meta http-equiv="X-Ua-Compatible" content="IE=edge,chrome=1">
Atrybut content powinien mieć wartość IE=edge, z opcjonalnym chrome=1. Można też określić konkretną wersję standardów IE, wpisując na przykład IE=10. Pełną dyskusję znajdziesz tutaj – zachęcam do lektury.

Podpięcie (zainkludowanie) arkusza stylów CSS:

<script src="code.js"></script>
Atrybut: type="text/javascript" jest opcjonalny, a nawet zbędny w HTML 5, aczkolwiek jego wstawienie nie jest błędem. Więcej szczegółów na ten temat znajdziesz w tej dyskusji. Ponownie, nie zapomnij o prostym teście prawidłowego podpięcia skryptu – wystarczy jeden mały alert w pliku JS aby przekonać się, że kod JS rzeczywiście jest interpretowany przez przeglądarkę. Uwaga: w samym pliku z rozszerzeniem JS nie trzeba już pisać tagów <script>.

Na koniec wspomnijmy jeszcze o dyskusji na temat domykania tagów w HTML 5 w porównaniu do XHTML i HTML 4.01 – czy należy kończyć pojedyncze znaczniki znakiem / czy nie? Czyli czy powinno się zapisać:

<meta charset="utf-8">
czy jednak:

<meta charset="utf-8" />
