
### Cel projektu

Celem projektu jest analiza przepływu ciepła w pomieszczeniach oparta na równaniu ciepła. Jest to cząstkowe równanie różniczkowe pozwalające precyzyjnie opisać rozkład temparatury w czasie i przestrzeni w zależności między innymi od źródła ciepła oraz  strat związanych z temperaturą na zewnątrz.

Rozważymy dwa główne problemy:

**Gdzie najlepiej ustawić grzejniki?**

Popularnym rozwiązaniem jest zlokalizowanie ich pod oknami. Poddamy analizie efektywność takiego rozwiązania. Porównamy również to, czy temperatura rozkłada się równomiernie oraz jakie straty ciepła ponosimy w zależności od tego, gdzie ustawimy źródła ciepła.

**Czy opłaca się zakręcać grzejniki wychodząc z domu?**

Wydawać by się mogło, że kiedy opuszczamy pomieszczenie, możemy ogrzewać je w mniejszym stopniu i zaoszczędzić. W tym czasie jednak temperatura spadnie i kiedy wrócimy, będziemy chcieli dogrzać pokój na nowo do komfortowej temperatury. Przetestujemy, czy takie rozwiązanie przynosi nam oszczędność względem sytuacji, kiedy utrzymujemy stałą temperaturę pomieszczenia.

### Założenia
Do analizy rozkładu ciepła potrzebujemy kilku istotnych założeń


*   Temperatura na oknie wynosi tyle samo, co temperatura zewnętrzna
*   Rozkład dobowy temperatur podzielimy na 3 poziomy: chłodno (między $ 8^o $ C a $ 15^o $ C), zimno ( $ 0^o $ C do $ 8^o $ C) i bardzo zimno ( $ -10^o $ C do $ 0^o $ C) Dokładne dane zostaną wygenerowane przy pomocy Chat GPT do trzech plików typu .csv, gdzie również znajdą się te temperatury przeliczone na stopnie Kelwina oraz podziałka godzinowa (24h podzielone na przedziały o długości 3 minuty)
*   Ściany izolują nam temperaturę, temperatura na nich wynosi tyle samo co temperatura obok nich.
* Wszystkie grzejniki w analizowanym mieszkaniu mają moc 800 W.
* Za komfortową temperaturę przyjmujemy $ 21^oC $ .
* Stosujemy termostaty tzn po osiągnięciu pewnej temperatury ogrzewanie wyłącza się. Mierzyć będziemy temperaturę w jednym punkcie w centrum pomieszczenia. Ustawiamy temperaturę na termostacie na $21^oC$. Gdy temperatura w tym punkcie osiągnie $21^oC$ - grzejniki w pomieszczeniu wyłączą się automatycznie. Gdy temperatura spadnie - włączą się ponownie.
* Drzwi w pomieszczeniu są otwarte i mają grubość dwóch kratek w podziałce - po jednej na każde z pomieszczeń, które łączą. Temperatury z pomieszczenia X oraz pomieszczenia Y na sąsiadujących kratkach uśredniamy.
* Drzwi oraz okna są fragmentami ścian, natomiast grzejniki znajdują się obok nich, w pomieszczeniu.
* Ciepło właściwe powietrza wynosi $c=1005 \frac{J}{kg*K}$
* Gęstość powietrza wynosi $1,2 kg/(m^3)$

