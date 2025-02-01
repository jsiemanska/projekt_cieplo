# Analiza ogrzewania w budynkach

## Wstęp
Celem projektu jest analiza przepływu ciepła w pomieszczeniach oparta na równaniu ciepła. Jest to cząstkowe równanie różniczkowe pozwalające precyzyjnie opisać rozkład temparatury w czasie i przestrzeni w zależności między innymi od źródła ciepła oraz strat związanych z temperaturą na zewnątrz. W szczególności interesuje nas, jak różne strategie ogrzewania wpływają na oszczędność energii oraz komfort cieplny.


## Model matematyczny
Przyjęliśmy model przewodnictwa cieplnego opisany równaniem różniczkowym:

$$
\frac{\partial u}{\partial t} = \alpha \Delta u + \frac{P}{\rho A c} \Theta(x, u)
$$

gdzie:
- $u(x,t)$ – temperatura w punkcie $x$ w czasie $t$,
- $\alpha$ – współczynnik przewodnictwa cieplnego,
- $P$ – moc grzejnika,
- $\rho$ – gęstość powietrza,
- $A$ – powierzchnia,
- $c$ – ciepło właściwe.

### Założenia
Do analizy rozkładu ciepła potrzebujemy kilku istotnych założeń


*   Temperatura na oknie wynosi tyle samo, co temperatura zewnętrzna
*   Rozkład dobowy temperatur podzielimy na 3 poziomy: chłodno (między 8°C a 15°C), zimno (0°C do 8°C) i bardzo zimno (-10°C do 0°C) Dokładne dane zostaną wygenerowane przy pomocy Chat GPT do trzech plików typu .csv, gdzie również znajdą się te temperatury przeliczone na stopnie Kelwina oraz podziałka godzinowa (24h podzielone na przedziały o długości 3 minuty)
*   Ściany izolują nam temperaturę, temperatura na nich wynosi tyle samo co temperatura obok nich.
* Wszystkie grzejniki w analizowanym mieszkaniu mają moc 800 W.
* Za komfortową temperaturę przyjmujemy 21 stopni.
* Stosujemy termostaty tzn po osiągnięciu pewnej temperatury ogrzewanie wyłącza się. Mierzyć będziemy temperaturę w jednym punkcie w centrum pomieszczenia. Ustawiamy temperaturę na termostacie na 21 stopni. Gdy temperatura w tym punkcie osiągnie tyle - grzejniki w pomieszczeniu wyłączą się automatycznie. Gdy temperatura spadnie do - włączą się ponownie.
* Drzwi w pomieszczeniu są otwarte i mają grubość dwóch kratek w podziałce - po jednej na każde z pomieszczeń, które łączą. Temperatury z pomieszczenia X oraz pomieszczenia Y na sąsiadujących kratkach uśredniamy.
* Drzwi oraz okna są fragmentami ścian, natomiast grzejniki znajdują się obok nich, w pomieszczeniu.
* Ciepło właściwe wynosi $c=1005 \frac{J}{kg*K}$
* gęstość powietrza wynosi $\rho=1.2 \frac{kg}{m^3}$

## Problemy
Przeprowadziliśmy szczegółowe symulacje dla różnych scenariuszy, analizując zmiany temperatury w funkcji czasu i miejsca.


**Gdzie najlepiej ustawić grzejniki?**

Popularnym rozwiązaniem jest zlokalizowanie ich pod oknami. Poddamy analizie efektywność takiego rozwiązania. Porównamy również to, czy temperatura rozkłada się równomiernie oraz jakie straty ciepła ponosimy w zależności od tego, gdzie ustawimy źródła ciepła.
- Wykonaliśmy dwie symulacje: w pierwszej grzejnik znajdował się pod oknem, w drugiej na przeciwległej ścianie.
- Wyniki pokazały, że umiejscowienie grzejnika wpływa na równomierność rozkładu temperatury. Grzejnik pod oknem powoduje większe różnice temperatur, ale jednocześnie lepiej przeciwdziała utracie ciepła przez okna.
- 
**Czy opłaca się zakręcać grzejniki wychodząc z domu?**

Wydawać by się mogło, że kiedy opuszczamy pomieszczenie, możemy ogrzewać je w mniejszym stopniu i zaoszczędzić. W tym czasie jednak temperatura spadnie i kiedy wrócimy, będziemy chcieli dogrzać pokój na nowo do komfortowej temperatury. Przetestujemy, czy takie rozwiązanie przynosi nam oszczędność względem sytuacji, kiedy utrzymujemy stałą temperaturę pomieszczenia.
- Porównaliśmy zużycie energii w przypadku pozostawienia ogrzewania włączonego na niskim poziomie oraz całkowitego wyłączania grzejników przed wyjściem.
- W analizie uwzględniono różne warunki atmosferyczne: chłodno, zimno oraz bardzo zimno.
- Wyniki wykazały, że w przypadku umiarkowanych temperatur bardziej opłacalne jest zostawienie ogrzewania na minimalnym poziomie, natomiast w skrajnie niskich temperaturach oszczędności są niewielkie.

## Wizualizacje
Rozważając temperaturę na poziomie "chłodno" otrzymujemy następujące mapy ewolucji ciepła w zależności od ustawienia grzejników pod oknami lub na przeciwległych ścianach:

![Wykres temperatury](animacja.gif)

![Wykres temperatury](animacja4(1).gif)

Biorąc pod uwagę poziom temperatury "zimno", wygląda to następująco:


![Wykres temperatury](animacja2.gif)

![Wykres temperatury](animacja5.gif)

Natomiast na poziomie "bardzo zimno":

![Wykres temperatury](animacja3.gif)

![Wykres temperatury](animacja6.gif)
