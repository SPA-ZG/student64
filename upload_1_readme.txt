URL aplikacije u cloudu:
	https://currencies-converter-rates.vercel.app/

Svojstva aplikacije:
	1. interpolation/one-way binding -> Napravljeno. Moguće vidjeti unutar npr. src/components/RateCard.vue (linije 34 i 35) te src/components/CurrencyConverter.vue (linije 141 - 145).
	2. two-way binding -> Napravljeno. Moguće vidjeti unutar npr. src/components/CurrencyConverter.vue (linije 111 i 112 gdje se za binding u jednom smjeru koristi :value, a za binding u drugom smjeru se koristi @input) te src/components/CurrencySelection.vue (linija 42 gdje se koristi v-model).
	3. methods -> Napravljeno. Moguće vidjeti unutar npr. src/components/CurrencyConverter.vue (linije 23 - 77).
	4. computed properties -> Napravljeno. Moguće vidjeti unutar src/components/CurrencySelection.vue (linije 21 - 30).
	5. barem jedan scoped style -> Napravljeno. Moguće vidjeti unutar npr. src/views/RatesView.vue (linije 89 - 113).
	6. koristiti barem jedan lifecycle hook -> Napravljeno. Moguće vidjeti unutar npr. src/views/RatesView.vue (linije 17 - 19 gdje se koristi mounted() lifecycle hook).
	7. routing (više stranica) -> Napravljeno. Moguće vidjeti unutar src/router/index.js (linije 7 - 19). Definirana je ruta / i ruta /rates.
		- aplikacija mora biti bookmarkable, tako da rade linkovi (ne samo na root, već i moj-web.com/stranica1, moj-web.com/stranica2) -> Napravljeno. Moguće vidjeti unutar vercel.json i isprobati upisivanjem linka https://currencies-converter-rates.vercel.app/rates u address bar preglednika.
		- dinamičko usmjeravanje s 404 stranicom ("catch all") -> Napravljeno. Moguće vidjeti unutar src/router/index.js (linije 20 - 25) i isprobati upisivanjem linka https://currencies-converter-rates.vercel.app/ratess u address bar preglednika.
	8. (barem) dvije komponente -> Napravljeno. Moguće vidjeti unutar src/components foldera
	9. barem jedna komponenta mora emitirati barem jedan event -> Napravljeno. Moguće vidjeti unutar src/components/CurrencySelection.vue (linije 26 - 28 i 31 - 36).
	10. store (Pinia) -> Napravljeno. Moguće vidjeti unutar src/stores/converter.js gdje je store definiran i unutar src/components/CurrencyConverter.vue gdje se store koristi za globalnu pohranu odabranih valuta te unesene i izračunate vrijednosti pretvorbe.
	11. asinkroni dohvat podataka s backenda -> Napravljeno. Moguće vidjeti unutar npr. src/views/RatesView.vue (linije 21 - 36). Koristi se https://app.exchangerate-api.com/ za dohvat podataka.

Za pokretanje projekta lokalno prvo je potrebno izvesti naredbu "npm i" kako bi se instalirali svi potrebni paketi, a potom se aplikacija pokreće naredbom "npm run dev".
