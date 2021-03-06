1.  `C-x C-SPC`: Hoppar till förra stället du var på i koden. T.ex. om
	du har sökt dig till ett ställe i koden för att hämta upp/kopiera
	någon bit information eller göra någon relaterad ändring kan du
	snabbt ta dig tillbaka igen.

2.  `C-x C-x`: Hoppar till punkten i koden du nyss var på, men byter
	plats på denna och utgångspunkten i minnet. Upprepade C-x C-x
	hoppar alltså fram och tillbaka mellan två punkter i koden.

	Bra för om man menade att markera det område mellan där en sökning
	utgick ifrån och där sökningen landade, men glömde det. Då kan man
	göra C-SPC C-x C-x och så har man markerat området.

3.  `C-s C-s` eller `C-r C-r`: Söker på det senast sökta sökordet
	igen.

4.  `C-s sökord C-g`: Går till nästa förekomst av sökord och sedan
	tillbaka utan att flytta markören. Bra för att kolla upp
	t.ex. tidigare användningar av en variabel för att sedan fortsätta
	skriva utan att behöva orientera sig i koden igen.

5.  `C-s söko C-w`: Kompletterar söktermen till slutet på ordet som
	pekaren står vid. Så har du börjat skriva in `söko` och pekaren
	därmed står likt `söko|rd` blir söktermen `sökord` när du trycker
	`C-w`.

	Kan användas som en fattig mans diff mellan två närliggande delar
	av en text, bara trycka ner `C-w` tills den andra delen inte
	längre matchar.

6.  `C-SPC` följt av markeringen av en region samt `C-_` kör undo,
    fast bara i den markerade regionen.

7.  `M-x term` startar upp en fullvärd smart terminal i vilken man kan
    köra program som vill skriva om hela terminalytan, t.ex. less,
    htop, git grep eller varför inte emacs. Detta till skillnad från
    `M-x shell` eller `M-x eshell` som startar så kallade dumma
    terminaler.

    Eftersom att term-mode sänder alla tecken till skalet per default,
    likt screen, behövs det en flyktsekvens: `C-c`. `C-c` sänder `C-x`
    till den ovanliggande emacsprocessen så `C-x o` blir i term-mode
    `C-c o`.

8.  `C-x h` markerar hela buffern.

9.  `M-<` går till början av buffern, `M->` går till slutet av buffern.

10. Emacs har en inbyggd profilerare för sig själv. Så skulle du finna
    att någonting går långsammare än det borde kan du alltid skriva
    `M-x profiler start`, göra saken som är ovanligt seg och avsluta
    det hela med `M-x profiler-report`.

11. Tramp låter dig ansluta till och läsa filer på system som inte har
    emacs. T.ex. kan du med paketet [docker-tramp] installerat ansluta
    till dockerbehållare på din lokala maskin och ändra filer utan att
    behöva häda.


	[docker-tramp]: https://github.com/emacs-pe/docker-tramp.el
