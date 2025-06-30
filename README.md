# Arbitru, viewer și exemplu de agent pentru jocul Quarto

Acest set de unelte vă permite să creați un program (agent) pentru jocul [Quarto](https://en.wikipedia.org/wiki/Quarto_(board_game)) și să organizați partide contra altor programe.

## Agenții

[Agenții](https://github.com/nerdvana-ro/quarto-tools/tree/main/agents) sînt programe care joacă Quarto. Agenții citesc starea jocului și tipăresc o mutare.

Repoul include cîțiva agenți, dintre care [Squarehead](https://github.com/nerdvana-ro/quarto-tools/tree/main/agents/squarehead) joacă corect (dar modest). Restul agenților (Error, Hang etc.) se comportă anormal și au rolul de a testa buna funcționare a arbitrului.

## Arbitrul

[Arbitrul](https://github.com/nerdvana-ro/quarto-tools/tree/main/arbiter) organizează partide între doi agenți. Arbitrul ține evidența jocului și invocă pe rînd fiecare agent, comunicîndu-i starea curentă. Apoi citește răspunsul agentului și actualizează starea jocului.

Arbitrul poate organiza și turnee cu mai multe partide.

## Viewerul

[Viewerul](https://github.com/nerdvana-ro/quarto-tools/tree/main/viewer) redă o partidă mutare cu mutare, într-un mediu grafic. El este scris în HTML + Javascript + CSS, deci trebuie deschis într-un browser.

## Pași de urmat

Vă recomand să încercați uneltele în această ordine:

* **Testați arbitrul**: Faceți instalările și configurările necesare pentru a organiza o partidă între două copii ale agentului Squarehead.
  * Dacă rulați Windows, va fi nevoie să instalați WSL. Și acest pas este documentat în secțiunea despre arbitru.
* **Testați viewerul**: Încărcați în viewer o partidă salvată și derulați prin ea.
* **Învățați strategia jocului:** Quarto nu este un joc dificil, dar oamenii pot fi ușor derutați. Vă recomand să jucați cel puțin 5 partide între voi, ca să descoperiți ce merge și ce nu merge. Desigur, puteți citi și opinii de pe Internet.
* **Scrieți un client:** De aceea ne-am adunat aici! 😉 Urmați specificațiile din [protocol.md](https://github.com/nerdvana-ro/quarto-tools/blob/main/protocol.md).

Scopul final al acestei săptămîni este să scrieți un client care să bată cît mai convingător agentul Squarehead.

Desigur, vom avea și un turneu final (vom decide formatul miercuri sau joi). Dacă vă clasați onorabil în acel turneu, cu atît mai bine!

## Cîteva cuvinte despre Squarehead

Strategia lui Squarehead este _greedy_ la o mutare înainte.

* Dacă poate cîștiga cu piesa din mînă, cîștigă.
* Altfel, caută la întîmplare o poziție de amplasat și o piesă de oferit astfel încît adversarul să nu poată cîștiga la următoarea mutare.

TODO: Descrie mărimea codului.
