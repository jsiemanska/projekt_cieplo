Celem projektu jest analiza przepływu ciepła w pomieszczeniach oparta na równaniu ciepła. 
W pliku projekt_cieplo.pdf znajdują się opisy do otrzymanych wyników.
Pliki z animacjami przedstawiają ewolucję map ciepła 
Przeprowadziliśmy szczegółowe symulacje dla różnych scenariuszy, analizując zmiany temperatury w funkcji czasu i miejsca.


**Gdzie najlepiej ustawić grzejniki?**

Popularnym rozwiązaniem jest zlokalizowanie ich pod oknami. Poddamy analizie efektywność takiego rozwiązania. Porównamy również to, czy temperatura rozkłada się równomiernie oraz jakie straty ciepła ponosimy w zależności od tego, gdzie ustawimy źródła ciepła.
- Wykonaliśmy dwie symulacje: w pierwszej grzejnik znajdował się pod oknem, w drugiej na przeciwległej ścianie.
- Wyniki pokazały, że umiejscowienie grzejnika wpływa na równomierność rozkładu temperatury. Grzejnik pod oknem powoduje większe różnice temperatur, ale jednocześnie lepiej przeciwdziała utracie ciepła przez okna.
  

## Wizualizacje
Rozważając temperaturę na poziomie "chłodno" otrzymujemy następujące mapy ewolucji ciepła w zależności od ustawienia grzejników pod oknami lub na przeciwległych ścianach:

![Wykres temperatury](animacja.gif)
![Wykres temperatury](animacja4.gif)

Biorąc pod uwagę poziom temperatury "zimno", wygląda to następująco:

![Wykres temperatury](animacja2.gif)
![Wykres temperatury](animacja5.gif)

Natomiast na poziomie "bardzo zimno":

![Wykres temperatury](animacja3.gif)
![Wykres temperatury](animacja6.gif)

W każdym tym przypadku możemy zauważyć, że gdy umiejscawiamy grzejnik pod oknem, w pewnym momencie wyłącza się on, rozkład temperatury jest też bardziej równomierny. Gdy patrzymy na przypadki, gdzie grzejniki są na prostopadłych ścianach do okien, widzimy jak rozchodzi się ciepło wokół grzejnika oraz zimno od okna. Temperatura jest mało równomierna.

**Czy opłaca się zakręcać grzejniki wychodząc z domu?**

Wydawać by się mogło, że kiedy opuszczamy pomieszczenie, możemy ogrzewać je w mniejszym stopniu i zaoszczędzić. W tym czasie jednak temperatura spadnie i kiedy wrócimy, będziemy chcieli dogrzać pokój na nowo do komfortowej temperatury. Przetestujemy, czy takie rozwiązanie przynosi nam oszczędność względem sytuacji, kiedy utrzymujemy stałą temperaturę pomieszczenia.
Dla temperatury z zakresu "chłodno", przy wyłączaniu grzejnika na 6 godzin w ciągu dnia tzn od 10:00 do 16:00, zużywamy około 71% energii, którą zużylibyśmy zostawiając włączone kaloryfery. Gdy temperatura to "zimno", jest to około 80%, natomiast dla temperatur z zakresu "bardzo zimno" mamy już 92% energi użytej gdybyśmy grzejników nie wyłączali. 
Konkretne wartości jakie otrzymaliśmy to dla kolejnych poziomów temperatur i nie wyłączania
- Porównaliśmy zużycie energii w przypadku pozostawienia ogrzewania włączonego na niskim poziomie oraz całkowitego wyłączania grzejników przed wyjściem.
- W analizie uwzględniono różne warunki atmosferyczne: chłodno, zimno oraz bardzo zimno.
- Wyniki wykazały, że w przypadku umiarkowanych temperatur bardziej opłacalne jest zostawienie ogrzewania na minimalnym poziomie, natomiast w skrajnie niskich temperaturach oszczędności są niewielkie.
  
[14182.421227197432, 14792.703150912199, 15495.854063018345]
[10029.850746268694, 11820.895522388117, 14248.75621890556]
