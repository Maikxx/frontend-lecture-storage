# You don't know JS Samenvattingen

## You don't know JS - Up and Going - Hoofdstuk 1

Synoniemen voor programma: source code en code. Een set instructies die de computer vertellen welke taak deze moet uitvoeren.

De regels voor een valide format en gecombineerde instructies heet een computer taal of syntax.

Een groep woorden, nummers en operatoren die een bepaalde taak uitvoeren heten een statement. Statements eindigen op een semicolon.

Een statement bestaat uit één of meerdere expressions. Dit zijn referenties naar variabelen of waardes, of een set van variabelen of waardes, gecombineerd met operators.
Er zijn verschillende soorten expressions:
Literal value expression: 2
Variable expression: b
Arithmic expression / expression statement: b * 2
Assignment expression: a = b * 2
Call expression statement: alert(a)

Een programma moet worden uitgevoerd. Voordat dit kan moet het eerst worden geïnterpret en gecompiled naar computer leesbare code.

Het lezen van code regel voor regel heet interpreteren.
Soms werken talen zo, dat ze dingen van te voren af al vertalen naar computer leesbare code, dit heet compiling.

JS enginge compiles tegelijkertijd met dat het uitgevoerd wordt.

Om input te krijgen kan je forms gebruiken of de prompt() functie.

Als je een waarde aan een variabele assignt, berekent JS eerst de source value (rechterzijde van de statement).

Variabelen verklaren doe je met het keyword var.

Compound assignment: +=, -=, *=, /=.
Object property access: .
Loose-equals: ==
Strict-equals: ===
Loose-not-equals: !=
Strict-not-equals: !==
Less than or loose-equals: <=
Greater than or loose-equals: >=

Verschillende representaties van waardes heten types.
Waardes die direct in de source code worden opgenomen heten literals.

Het transformeren van waardes (nummer > string, vice versa) heet coercion.
Een voorbeeld hiervan is de Number() functie. Deze coersie (dwang) is een expliciete coersie.
Als je twee waardes van niet hetzelfde type vergelijkt is het een impliciete coersie.

Impliciete coersie is dubieus, maar je moet het wel kennen om te besluiten of je er gebruik van gaat maken of niet.

Binaire code komt vanuit compiling.

Het is belangrijk om namen van variabelen en functies duidelijk te formuleren. Ook zijn comments belangrijk. Schrijf hier niet te veel, maar ook niet te weinig van. Comments moeten uitleggen waarom en niet wat, maar soms ook hoe.

Een symbolische container om waardes in op te slaan: een variabele.
Als je een waarde vastzet in een type (string, number) heet dit static typing of type enforcement. Dit zorgt voor correctheid in de code.
Als je dat niet doet, krijg je weak typing, of dynamic typing. Dit zorgt voor flexibiliteit.
Het primaire doel van variabelen: de state van een programma onderhouden. State volgt dus de veranderingen die je programma doorlopen.

Het centraliseren van waardes heet constants. Deze variabelen mogen niet meer veranderen.
JS constant namen zijn geschreven met hoofdletters en _ tussen de woorden in. De nieuwe versie gebruikt het keyword const.

Een set samengevoegde statements heet een block. Deze zijn gewrapt in {}. Block statements hebben geen semicolons nodig.

Besluiten in programma’s worden genomen door conditionals.
If statement.
Else voorwaarde.
Switch statement.
Loops zijn ook in zekere zin een conditional, ze kijken namelijk of ze moeten lopen.

Een lege string en de waarde 0 zullen in een conditional false worden.

Het herhalen, terwijl de conditie waar is, wordt in programmeren loopen genoemd. Een loop bestaat uit een test conditie en een block code. Iedere keer als de code in het blok loopt, heet het een iteratie.

Verschil tussen while en do…while: bij een while loop wordt de conditie getest, nog voor de iteratie één keer gelopen is, bij de do…while is dat niet zo. Een do…while loop zal dus altijd één keer lopen.

Een for-loop heeft drie voorwaardes: initialization voorwaarde; conditional test voorwaarde; update voorwaarde.

Functies zijn in het leven geroepen om herhaling tegen te gaan. Functies kunnen parameters of argumenten met zich mee gepasst krijgen.

Een scope of lexical scope staat voor een collectie van variabelen, samen met de regels over hoe deze variabelen toegankelijk zijn, via hun naam. Er mogen geen twee dezelfde namen in een functie zitten. Scopes kunnen worden genest.
Lexical scope betekent dat de code in één scope toegang heeft tot variabelen binnen die scope, of die daarbuiten.

Recap:
Je hebt operatoren nodig om acties uit te voeren met waardes.
Je hebt waardes en types nodig om verschillende acties mogelijk te maken op de verschillende types.
Je hebt variabelen nodig om data (of state) in op te slaan, gedurende de executie van het programma.
Je hebt conditionals nodig om beslissingen te maken.
Je hebt loops nodig om herhaaldelijk taken uit te voeren, totdat de condition false wordt.
Je hebt functies nodig om je code te organiseren in logische en herbruikbare delen.

## You don't know JS - Up and Going - Hoofdstuk 2

ECMASCRIPT is de officiële naam voor de JavaScript specificatie.

Typeof null = object. (bug, die nooit gefixt zal worden, in verband met creëren nieuwe bugs).

Object properties zijn ook wel named locations genoemd. Properties kunnen worden bereikt via de dot notation of bracket notation.
Properties in de bracket notatie worden vaak keys genoemd.

Arrays en functies zijn een soort subtypes van objecten.
Gebruik arrays voor numeriek gepositioneerde waarden en objecten voor benaamde properties.

Functies kunnen ook properties hebben en worden bereikt via de dot notation, maar vaak is dit niet het geval.

Een String object form, of native wordt gekoppeld aan een primitief string type waarde. Hierdoor kan je properties op string etcetera roepen.

Er zijn twee hoofdelijke types van waarde vergelijking: equality en inequality. Hier komt altijd een boolean uit.

Equality:
Var a = “42”;
Var b = a * 1 — impliciete coersie tot het nummer 42.

Waardes die false zijn:
“” - lege string.
`0`, `-0`, `NaN`.
`Null`, `undefined`.
false.

`==` - Kijkt naar de waarde gelijkheid, met coersie toegestaan.
`===` - Kijkt naar de waarde gelijkheid, zonder dat coersie is toegestaan.

Bij a == b wordt de a waarde gelijk aan het type van b. (“42” -> 42).

Wanneer gebruik je == of ===?
Als minstens één van de kanten van de vergelijking false of true kunnen zijn. ===
Als minstens één van de waarde in een vergelijking gelijk kan zijn aan 0, “”, [ ]. ===
Alle andere momenten ==

Als je twee non-primitieve waardes vergelijkt, zoals objecten, moet je heel goed opletten op de == en ===.

Arrays worden standaard gecoerced naar strings, gescheiden met komma’s, zonder spaties. Twee arrays met dezelfde waarde aan elkaar vergelijken, levert geen true op.

Inequality:
`<`, `>`, `<=`, `>=` - Relational comparison.
Als je de waardes `32 < “42”` met elkaar vergelijkt komt hier true uit, omdat een van de waardes geen string is, worden beide waardes naar nummers omgezet.
Als je “42” < “43” vergelijkt komt hier true uit, omdat de waardes lexicografisch met elkaar worden vergelijken (op alfabetische waarde).

Strings die worden omgezet naar nummers worden NaN. Een NaN waarde is altijd groter dan of kleiner dan iedere andere waarde. Je kan hier dus niet mee vergelijken.

Variabele namen moeten valide identifiers zijn. Naam moet beginnen met a-z, A-Z, $, _. Het kan verder al deze dingen bevatten, plus de nummers 0-9.
Sommige woorden kunnen niet gebruikt worden als variabelen, maar wel als property namen. Dit zijn reverved words.

Als een variabele in een scope voorkomt, wordt deze verklaring gelijkgesteld aan de gehele scope en is ook toegankelijk overal in die scope. Dit heet hoisting. Een variabele die aangemaakt is, wordt naar de bovenkant van zijn scope verplaatst. Hoisted variabelen gebruiken is niet verstandig, maar met functies kan het wel.

Een variabele is toegankelijk in zijn scope en elke geneste scope.

In ES6 kun je variabelen aanmaken, op functie niveau met let.

```js
function foo() {
	var a = 1;

	if (a >= 1) {
		let b = 2;

		while (b < 5) {
			let c = b * 2;
			b++;

			console.log( a + c );
		}
	}
}
```

Hierin is b alleen beschikbaar in de if statement. Dit soort scoping heet block scoping.

Als je in een switch statement geen breaks gebruikt, terwijl die case matcht, zal de volgende case ook aangeroepen worden, ook al is de case niet waar. Dit heet falling through. Dit is soms gewenst.

Een andere vorm van een conditional is een conditional operator, beter bekend als de ternary operator. Het is korter dan een enkele if…else.

Strict mode versterkt de restricties van sommige regels van gedrag in JavaScript. Dit zorgt ervoor dat de code veiliger is en zich meer aan de richtlijnen houdt. Het zorgt ook voor optimalisatie van de JS engine. Het zorgt ervoor dat er niet meer een globale variabele aangemaakt wordt als je een keyword vergeet. Strict mode wordt ook gezien als de toekomst van de taal.

Function foo() {} is simpelweg een variabele in de globale scope, met een referentie naar zichzelf (een functie). Een functie kan een waarde vertegenwoordigen, die aan andere variabelen of functies kan worden toegewezen.

Anonymous function expression: var funct = function() {}.
Named function expression: var funct = function func() {}. Dit heeft de voorkeur.

Immediately Invoked Function Expressions (IIFEs)
(function IIFE () {console.log(“Hello World”)})();
De omringende ( ) heeft JS nodig om het onderscheid te kunnen maken met een normale function call.
IIFEs creëren een eigen variabele scope, waardoor dezelfde namen binnen en buiten de functie gebruikt kunnen worden.
IIFEs kunnen ook dingen returnen.

Closure
Dit is een manier om te onthouden en toegang te kunnen blijven houden tot de variabelen van de scope van een bepaalde functie, als de functie klaar is met uitvoeren.

```js
function makeAdder(x) {
	// parameter `x` is an inner variable

	// inner function `add()` uses `x`, so
	// it has a "closure" over it
	function add(y) {
		return y + x;
	};

	return add;
}

// `plusOne` gets a reference to the inner `add(..)`
// function with closure over the `x` parameter of
// the outer `makeAdder(..)`
var plusOne = makeAdder( 1 );

// `plusTen` gets a reference to the inner `add(..)`
// function with closure over the `x` parameter of
// the outer `makeAdder(..)`
var plusTen = makeAdder( 10 );

plusOne( 3 );		// 4  <-- 1 + 3
plusOne( 41 );		// 42 <-- 1 + 41

plusTen( 13 );		// 23 <-- 10 + 13
```

De meest bekende plek om closures te gebruiken is via het module pattern.
Modules laten je privé implementatie details (zoals variabelen en functies) aanmaken, die van de buitenwereld zijn afgesloten, maar ook een public api, die toegankelijk is vanaf de buitenkant.

```js
function User(){
    var username, password;

	function doLogin(user,pw) {
		username = user;
		password = pw;

		// do the rest of the login work
	}

	var publicAPI = {
		login: doLogin
	};

	return publicAPI;
}
```

// create a `User` module instance

```js
var fred = User();

fred.login( "fred", "12Battery34!" );
```

Als je User ( ) doet, creëer je een instance van de User module. Dit is in feite een kopie, met een nieuwe scope.
Doordat via de publicAPI login is geëxporteerd, zijn de variabelen username en password niet verloren geraakt, nadat de functie klaar was.

This is niet altijd gerelateerd aan object-oriented patterns. Als een functie een this bevat, slaat deze vaak op een object. This refereert niet naar de functie zelf.

```js
function foo() {
	console.log( this.bar );
}

var bar = "global";

var obj1 = {
	bar: "obj1",
	foo: foo // Referentie naar de functie foo.
};

var obj2 = {
	bar: "obj2"
};

// --------

foo();                // “global” // In strict mode geeft dit een undefined error.
obj1.foo();            // "obj1"
foo.call( obj2 );        // "obj2"
new foo();            // undefined
```

Als je een property van een object probeert te refereren, die niet bestaat, zal JS automatisch de interne prototype van dat object gebruiken, om een ander object op te zoeken, waar die property wel opstaat.

```js
var foo = {
    a: 42
};

// create `bar` and link it to `foo`
var bar = Object.create( foo );

bar.b = "hello world";

bar.b;        // "hello world"
bar.a;        // 42 <-- delegated to `foo`
```

Dit systeem wordt vaak gebruikt en misbruikt om het te laten lijken op een class met inheritance.
Het beste patroon waarvoor dit gebruikt kan worden is behaviour delegation. In deze situatie bouw je je objecten, zodat ze opzettelijk worden afgevaardigd van het hoofdobject.

Er zijn twee dingen die je kunt doen om nieuwe features begrijpbaar te maken voor oudere browsers: polyfilling en transpiling.

Een polyfill refereert naar het pakken van een stuk nieuwe JS code en dat omzetten tot code met hetzelfde gedrag, dat beschikbaar is in de oudere JS omgevingen.

NaN waardes zijn de enige waardes die nooit gelijk zijn aan zichzelf.

Transpiling: een proces dat nieuwe code omzet naar oudere varianten van die code. Het transformeert de code en compiled deze. Transpiling gebeurt in het build-proces.

Waarom zouden we transpilen?:
* Nieuwe syntax maakt je code leesbaarder en onderhoudsarmer.
* Als je de getranspilede code alleen gebruikt voor oudere browsers en de nieuwe serveert aan de nieuwere browsers, kun je gebruik maken van de performance optimalizations, die met de nieuwe syntax zijn meegebracht. Zorgt er ook voor dat browser makers meer echte code hebben om mee te testen.
* Geeft feedback aan het JS comité (TC39).

Undefined is de enige waarde die niet in een standaard parameter kan worden meegegeven.
Je moet altijd transpilen.

Bekendste non-JS JS: DOM API. Deze API is alleen beschikbaar in de browser. Hierin is document een belangrijk host object.

## You don't know JS - Up and Going - Hoofdstuk 3

JavaScript is geen interpreted language, wat betekent dat het niet gecompiled wordt. Het wordt wel degelijk gecompiled, maar bijna instant daarna wordt het geëxecute.

Een belangrijke uitwerking van closures wordt gedaan in het module pattern.

Delegation zorgt ervoor dat je weinig meer met classes en inheritance te doen hebt.

## You don't know JS - Scopes & Closures - Hoofdstuk 1

Belangrijkste mogelijkheid in iedere programmeertaal: de mogelijkheid om waardes op te kunnen slaan in variabelen en deze vervolgens later op te halen of te veranderen. Dit zorgt voor state in een programma.

De set regels, die gaan ver het opslaan van variabele in een bepaalde locatie en het vinden van deze variabele later heet scope.

In traditionele compiled-languages gaat een programma drie stappen door, voordat het kan worden uitgevoerd: compilation:

Tokenizing / Lexing: Het opdelen van strings karakters in betekenisvolle (voor de taal) delen, genaamd tokens. Witruimte kan soms worden meegenomen als een token. Het verschil tussen tokenizing en lexing, zit hem in het feit of de tokens stateless of stateful zijn. Als een token onderdeel is van een ander token, heet dat lexing.

Parsing: Een array van tokens wordt omgezet in een boom van geneste elementen, die collectief de grammatische structuur van het programma omvatten.
Deze boom heet AST: Abstract Syntax Tree.

Code-Generation: Het proces van het pakken van de AST en deze omvormen tot uitvoerbare code. Dit deel varieert per taal, platform enzovoorts. Dit proces zorgt er ook echt voor dat er een variabele wordt aangemaakt, dat opgeslagen wordt op het lokale geheugen en vervolgens dat daar een waarde aan wordt toegevoegd.

JavaScript engines hebben geen luxe, om er lang over te doen om te optimizen, omdat het niet een stap van te voren gebeurt.

JIT: Een truc van JS, om te lazy-compilen en hot-recompilen.

Een engine is verantwoordelijk voor de compilatie en uitvoering van een JS programma, vanaf het begin tot het einde.
Compiler: Parset en genereert de code.
Scope: Een lijst van alle variabele, met daarbij een set van strikte regels, die gaan over hoe deze toegankelijk zijn voor de huidig lopende code.

Scopes worden bepaalt door functies en blocks. Functie scope heet ook wel lexical scope.

* De compiler vraagt aan de scope of de variabele al bestaat in diezelfde scope, als dat zo is, zal deze verklaring van een variabele worden overgeslagen. Anders vraagt de compiler aan scope, om een nieuwe variabele aan te maken in die scope collectie.
* De compiler zorgt er dan voor dat er code is geproduceerd voor de engine, zodat deze later uitgevoerd kan worden. Als de code gerund wordt door de engine, vraagt deze eerst aan scope of er een variabele toegankelijk is in de huidige scope collectie, als dat zo is, gebruikt de engine deze variabele, anders kijkt engine ergens anders voor deze variabele.

LHS gaat over de declaratie van een statement. Draait om het vinden van de variabele.
RHS gaat over de waarde van een statement. ( / Als er een variabele aan de rechterkant van een statement staat.)

Ook als je waardes meegeeft aan via parameters, wordt er in die functie een LHS operatie gedaan, omdat de meegegeven waarde aan de parameternaam wordt gekoppeld.

Als een RHS faalt om een variabele te vinden, waar dan ook in de geneste scopes, geeft de engine een ReferenceError.

Als de engine een LHS aanvraag aan het doen is en het komt op de bovenste etage aan (globale scope), zonder deze variabele te vinden en het programma loopt niet in strict mode zal er in de globale scope een nieuwe variabele aangemaakt worden en teruggegeven worden aan de engine.
Strict mode zorgt ervoor dat er niet automatisch of impliciet variabelen aangemaakt kunnen worden op de bovenstaande manier. Ook dan zal de engine een ReferenceError geven.

Als je een RHS aanvraag doet, maar de waarde komt niet overeen met wat je er mee probeert ermee te doen, zal de engine een andere error geven: TypeError.

## You don't know JS - Types & Grammar - Hoofdstuk 1

ES types:
Undefined
Null
Boolean
String
Number
Object
Symbol

Een type is (in JavaScript) een intrinsieke, ingebouwde set karakteristieken, die op een unieke manier het gedrag, van een gegeven waarde identificeert en onderscheidt van andere waardes, voor de engine én de developer.

Alle types, behalve objecten heten primitives.

Null is de enige primitieve waarde, die falsy is.

Een function is een subtype van een object. Het is een aanroepbaar object.
De length property van een function komt overeen met de hoeveelheid benoemde parameters.

Ook arrays zijn subtypes van objecten.

In JS hebben de variabelen geen types, maar juist de waardes.
JS heeft dus geen type enforcement.

typeof over een variabele aanroepen geeft de waarde van die variabele terug.

Variabelen die op dit moment geen waarde hebben, returnen undefined.

Undeclared en undefined zijn twee verschillende dingen. Undeclared betekent dat er geen variabele is aangemaakt in de toegankelijke scope.

typeof returnt undefined, ook als er iets undeclared is.

Als je een property van een object probeert te refereren, terwijl deze onverklaard is, zal er geen ReferecError worden gegooid.

Dependency injection:
In plaats van gokken of er iets globaal is verklaard, kan je er voor zorgen dat mensen per se een variabele meegeven aan je functie:

```js
function doSomethingCool(FeatureXYZ) {
var helper = FeatureXYZ ||
function() { /*.. default feature ..*/ };

var val = helper();
}
```

## You don't know JS - Types & Grammar - H2

Bouwstenen van iedere taal: arrays, strings en numbers. JavaScript heeft hier enkele unieke karakteristieken aan verbonden.

Arrays in arrays worden multidimensionale arrays genoemd.

Als je in arrays genummerde waardes overslaat bij het toevoegen (0 > 2), dan wordt dat een sparse array. Hierin is de tweede waarde (1) undefined.

Je kan ook string keys/properties aan arrays toevoegen, die zullen niet meetellen aan de length property van de array.

Als een string waarde, bedoeld als een key, met een base-10 nummer waarde in de string, gaat een array er vanuit dat je bedoelde dat het nummer wou hebben.

Strings worden vaak gezien als arrays van karakters, echter zijn ze totaal anders.
JS strings zijn immutable, terwijl arrays wel mutable zijn.

Arrays hebben een reverse methode.
De meest gebruikte methode om strings te reversen, is door ze in een array om te zetten, te reversen en vervolgens weer terug naar een string om te zetten.

JS nummers bevatten beide integer en decimale nummers.
De implementatie waarop JS zijn nummer systeem heeft gebaseerd heet IEEE754, vaak ook floating-point genoemd. JS gebruikt daarvan het double precision (64-bit binary) format van die standaard.

Hele grote nummers worden automatisch omgezet naar de exponentiële vorm van dat nummer. Dit is hetzelfde als .toExponential( ) op een getal aanroepen.

De .toFixed( ) prototype functie van het Number object, zorgt ervoor dat je kan zien op hoeveel decimalen een nummer echt eindigt:

```js
Var a = 42.42.
a.toFixed(4); // “42.4200”
```

De .toPrecision( ) methode doet iets soortgelijks, maar kijkt dan naar hoeveel significante getallen aanwezig moeten zijn om een waarde te representeren. De waardes die uit deze functie komen zijn string representaties.

```js
42..toFixed(4); // Dit is een correcte functie call.
42 .toFixed(3); // Ook dit is valide.
```

Numerieke waardes kunnen ook in andere vormen worden uitgelegd: binary, octal, hexadecimal.
De octale waarde 0363 is sinds ES6 + strict mode niet meer toegestaan.
De nieuwe vormen, die wel valide zijn: 0o363 en 0O363. Gebruik echter altijd de lowercase o.

Het meest bekende side effect van binary floating-point numbers (niet alleen in JS) is dat:

```js
0.1 + 0.2 === 0.3 // False
```

Dit komt doordat het antwoord: 0.30000000000000004 is.
Integers hebben dit probleem niet.

De meest geaccepteerde manier om met deze rounding error om te gaan, is door een kleine waarde te gebruiken als tolerantie voor deze vergelijking. Deze waarde heet machine epsilon, 2^-52. In ES6 is dit nummer ingebouwd als property op het Number object, .EPSILON.

De maximale floating-point waarde is Number.MAX\_VALUE en de minimale floating-point waarde is Number.MIN_VALUE.

Het hoogst veilig te gebruiken integer getal is: 2^53 -1. In ES6: Number.MAX\_SAFE\_INTEGER en Number.MIN\_SAFE_INTEGER.
Deze waardes worden vaak alleen geraakt als je werkt met 64-bit ID’s van databases. Deze kunnen dus niet als getal worden opgeslagen, maar wel als string.

Sinds ES6 kan je checken of een variabele een integer is, met Number.isInteger( ).
Je kan ook testen of een nummer een safe integer is, met Number.isSafeInteger( ).

Om een nummer te forceren, dat het een 32-bit integer waarde wordt, gebruik je a | 0. Dit werkt, omdat de | bitwise operator alleen werkt voor 32-bits getallen.

Null is een lege waarde. Had een waarde, maar nu niet meer. Dit is een special keyword.
Undefined is een missende waarde. Heeft geen waarde gehad nog. Undefined is een identifier.

Een andere manier om de undefined waarde te krijgen is, met behulp van de void operator.
Als je ergens een waarde graag undefined wilt hebben, kun je dus de void operator gebruiken.

Als je twee niet nummers aan elkaar probeert te koppelen in een operation, krijg je een NaN. Not a Number. NaN is nooit gelijk aan een andere NaN. Je kan testen of een waarde NaN is met isNaN( ). Dit heeft echter een probleem, dat het ook true returnt als je string eraan meegeeft.
Je kan ook checken of een waarde niet gelijk is aan zichzelf, aangezien NaN de enige variant binnen JS is, waar dat het geval is.

Als je var a = 1 / 0 doet, krijg je Infinity. Hier is een positieve (POSITIVE\_INFINITY) en een negatieve (NEGATIVE_INFINITY) variant van.

Een negatieve 0 waarde kan je alleen vinden als 0 deelt door of vermenigvuldigt met een negatieve waarde. Als je dit om zet naar een string werkt het niet, dan wordt er gewoon een string met 0 en geen min gegeven. Als je het reversed (vanuit een string naar number) werkt het wel.
Ook als je vergelijkingen doet met 0 en -0, zal dit true teruggeven.

Om de speciale gelijkheid van -0 en NaN te vergelijken kan je sinds ES6 gebruik maken van object.is( ). Gebruik dit alleen bij deze twee cases.

In JS kan je geen referentie hebben van een variabele in een andere variabele. Een referentie richt zich op een (gedeelde) waarde.

```js
var a = 2;
var b = a; // `b` is always a copy of the value in `a`
b++;
a; // 2
b; // 3

var c = [1,2,3];
var d = c; // `d` is a reference to the shared `[1,2,3]` value
d.push( 4 );
c; // [1,2,3,4]
d; // [1,2,3,4]
```

Simpele waardes (scalar primitives) zijn altijd kopieën. (null, undefined, string, number, boolean, symbol).
Compound values (samengestelde waardes) maken altijd een kopie, met een referentie naar het oorspronkelijke object. (objects, functions en arrays)

```js
function foo(x) {
    x.push( 4 );
    x; // [1,2,3,4]

    // later
    x = [4,5,6];
    x.push( 7 );
    x; // [4,5,6,7]
}

var a = [1,2,3];

foo( a );

a; // [1,2,3,4]  not  [4,5,6,7]
```

Als je dit gedrag (manual object wrapper) niet wilt hebben moet je x leegmaken met x.length = 0 en vervolgens je gewenste variabelen hierin pushen.

Slice( ) zonder parameters maakt een (shallow) kopie van een array. Hierdoor kan de kopie niet de oorspronkelijke array aanpassen.

```js
function foo(x) {
    x = x + 1;
    x; // 3
}

var a = 2;
var b = new Number( a ); // or equivalently `Object(a)`

foo( b );
console.log( b ); // 2, not 3
```

Het probleem hiermee (boxed object wrappers) is, dat de onderliggende scalar primitive waarde niet mutable is.

## You don't know JS - Types & Grammar - H3

Ingebouwde types heten natives.

De meest bekende natives:

```js
String( )
Number( )
Boolean( )
Array( )
Object( )
Function( )
RegExp( )
Date( )
Error( )
Symbol( )
```

Natives zijn eigenlijk ingebouwde functies.

Als je ze aanroept als constructor functie, dan zal typeof een object teruggeven, maar instanceof geeft wel de juiste native.

Via de constructor functie instanties aanmaken levert een wrapper object op van dat type, niet de primitieve waarde, die je wellicht bedoelde.

Er zijn geen Null en Undefined native constructors.

Voor de andere primitieve waarde, zoals strings, booleans en numbers, gebeurt er iets dat boxing heet.

Primitieve waardes hebben geen methodes of properties, hiervoor heb je een object wrapper nodig. JS doet dit automatisch.

Als je bijvoorbeeld var a = new Boolean (false) doet, zal dit alsnog true returnen in een vergelijking, omdat er een object omheen zit.

Als je wel een object wrapper hebt en je wilt de onderliggende waarde hebben, kun je gebruik maken van:

```js
.valueOf( )
```

Als je aan `Array()`, slechts een waarde meegeeft, wordt dat gezien als de lengte van de array.
Een array met minstens één lege slot, heet een sparse array.

`.apply()` is een utlity beschikbaar op alle functies, deze roept de functie op, waarmee het gebruikt wordt, maar op een speciale manier.

```js
Var a = Array.apply(null, {length: 3});
```

Bovenstaande maakt een array handmatig aan met drie x undefined.

Functie constructor is alleen hulpvol op sommige momenten, waar je dynamisch de functie parameters / diens functiebody moet bepalen.

Ook RegExps kun je beter in de literal form maken, in verband met performance.
Het is wel handig om dynamisch het patroon voor een regex te be	palen.

De Date en Error constructors zijn veel nuttiger dan de andere, omdat er geen literal form van is.

```js
new Date( ).getTime();
```

Het bovenstaande geeft een integer terug, wat het aantal miliseconde vertegenwoordigd sinds 1 januari 1970. Sinds ES6 kan je Date.now( ) gebruiken.

De `Error()` constructor gedraagt zich hetzelfde met het new keyword, als zonder.
Dit object gebruik je vaak in combinatie met de throw operator.

Symbols zijn speciale unieke (niet altijd) waardes, die gebruikt kunnen worden als properties op objecten, met weinig angst dat ze botsen.
Je mag bij deze constructor geen new keyword gebruiken.
Je gebruikt ze voornamelijk voor privé of speciale properties.

De String.prototype.(methode) zijn volgens de spec te vinden op String#methode. Geen enkele van deze methodes passen de string aan in place.

Function.prototype geeft een lege functie terug, net als dat Array.prototype dat doet. Dit is handig, om errors in zelf gedefineerde functies te voorkomen:

```js
function isThisCool(vals,fn,rx) {
    vals = vals || Array.prototype;
    fn = fn || Function.prototype;
    rx = rx || RegExp.prototype;

    return rx.test(
        vals.map( fn ).join( "" )
    );
}

isThisCool();        // true

isThisCool(
    ["a","b","c"],
    function(v){ return v.toUpperCase(); },
    /D/
);
```

Sinds ES6 is dit niet meer nodig.
Het zorgt wel voor Memory/CPU trashing.

Gebruik ook nooit `Array.prototype` die achtereenvolgend worden aangepast.