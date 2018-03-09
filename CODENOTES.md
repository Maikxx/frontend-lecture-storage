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
Het is wel handig om dynamisch het patroon voor een regex te bepalen.

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

## You don't know JS - Types & Grammar - H4

Het ombouwen van een waarde, van het ene type naar het andere heet vaak type casting, als het expliciet wordt gedaan en coercion als het impliciet gedaan wordt (door JS zelf, die volgt de regels op die gaan over hoe een waarde gebruikt mag en kan worden).

Eigenlijk wordt bij beide varianten gepraat over coercion, dus tegenwoordig heet het explicit coercion en implicit coercion.

```js
Var b = 42 + ‘’; // Implicit coercion
```

Het side effect van bovenstaande is dat 42 een string wordt.

Astract operations: internal-only operations.

### toString

toString maakt van waardes een string.
array.toString geeft een string vertegenwoordiging van de array terug, waar de waardes gescheiden zijn met een komma.

### JSON

JSON.stringify( ) zorgt ervoor dat waardes geschikt zijn, als JSON string waarde.
JSON-safe: Iedere waarde die op een correcte manier kan worden vertegenwoordigd in een JSON representatie.
JSON.stringify is geen directe vorm van coercion.

Illegale JSON waardes:

* Undefined
* Functions
* Symbols
* Objects met circular references (property referenties binnen een object structuur, die een nooit-eindigende cyclus creëren)

Als JSON in een array een invalide waarde vindt, vervangt deze de waarde met null. Als het op een object gebeurt, wordt die property verwijderd.

toJSON moet een JSON-safe representatie teruggeven, niet een JSON string.

Je kan ook een optioneel tweede argument meegeven aan JSON.stringify. Dit heet de replacer, dit kan een array of functie zijn.
Het wordt gebruikt om de recusive serialization van een object aan te passen, door een filter mechanisme te gebruiken, die aangeeft welke properties er wel en welke niet moeten worden geïnclude.

Als het een array is, moet het een array zijn van strings, die in de serialization mogen zitten van een object.

Als het een function is, zal het eens worden aangeroepen voor het object zelf, en verder iedere keer bij een property. Iedere keer wordt er een key en value aan meegegeven. Je kan een key skippen als je undefined returnt.

Een derde argument aan de functie stringify heet space en zorgt ervoor dat er een beter leesbare versie van een object uit komt. Het kan een nummer zijn of een string, waarvan de eerste tien karakters gelden als spacing.

### toNumber

True wordt 1, false wordt 0, undefined wordt NaN, null wordt 0.

```js
var a = {
    valueOf: function(){
        return "42";
    }
};

var b = {
    toString: function(){
        return "42";
    }
};

var c = [4,2];
c.toString = function(){
    return this.join( "" );// "42"
};

Number( a );// 42
Number( b );// 42
Number( c );// 42
Number( "" );// 0
Number( [] );// 0
Number( [ "abc" ] );// NaN
```

### toBoolean

1 en 0 zijn niet hetzelfde als true en false, echter kun je ze wel converteren van 1 > true en 0 > false.

Alle JS waardes kunnen in een van de twee categorieën vallen:
Waardes die false worden als ze omgezet worden naar een boolean.
Alle andere gevallen (true).

Falsy values list:

* Undefined
* Null
* False
* +0, -0, NaN
* “”

Falsy objects zijn niet slechts objecten die falsy waardes omringen.Een falsy object is een waarde, die lijkt op en zich hetzelfde gedraagt als een normaal
Object, maar als je ze naar een boolean coerced, zal het een false waarde worden.

Falsy objects werden gebruikt voornamelijk in legacy code. Zoals document.all, dit zal true returnen. Het zit niet in JS zelf, maar in de implementatie van oude browsers.

### Explicit Coercion

Dit is het converteren van een type, op een duidelijke en expliciete manier.

Strings <—> Numbers
Hiervoor gebruik je de ingebouwde String en Number functies. Hierbij gebruik je geen new. Je kan ook toString gebruiken, of +getal. Het laatstgenoemde heet een unary operator (operator met slechts één operand)

\- - maakt een positieve string ook een positief nummer.

### Date to number

Het meest gebruikte hiervoor is:

```js
Var timestamp = +new Date( );
```

Dit geeft het directe ‘nu’ moment terug in ms sinds 1970.
Je kan echter beter Date.now( ) gebruiken tegenwoordig.

### ~

De tilde operator (bitwise NOT) wordt vaak niet gebruikt, omdat het niet begrepen wordt. Deze voert eerst de ToInt32 functie uit en voert vervolgens een bitwise negation (het draait de gelijkheid van iedere bit om).

ToInt32 voert eerst een toNumber transformatie uit.
Soms als je bitwise operators gebruikt, met bepaalde nummers, zullen de waardes een andere nummer waarde hebben.

```js
~42;    // -(42+1) ==> -43
```

-1 heet een sentinel value, wat betekent: een waarde, die een arbitraire semantische betekenis heeft gekregen, binnen een set van soortgelijke waardes (nummers).

Deze waarde wordt bijvoorbeeld gebruikt bij het checken of een string een andere substring heeft, met indexOf( ). Deze geeft -1 terug, als er niks is gevonden en anders een 0-based index waar de substring begint.

```js
var a = "Hello World";

~a.indexOf( "lo" );            // -4   <-- truthy!

if (~a.indexOf( "lo" )) {	// true
    // found it!
}

~a.indexOf( "ol" );            // 0    <-- falsy!
!~a.indexOf( "ol" );        // true

if (!~a.indexOf( "ol" )) {    // true
    // not found!
}
```

### Truncating bits

Sommige developers gebruiken ~~ om het decimale deel van een nummer af te ronden.
Het lijkt op, maar is niet hetzelfde als Math.floor.
Eerst maakt deze operator van een getal een int32 en doet vervolgens een bitwise flip, waarna het nog een keer geflipt wordt. In principe voert deze operatie dus alleen ToInt32 uit.

```js
Math.floor( -49.6 );    // -50
~~-49.6;				// -49
```

### Parsing numeric strings

parseInt is een functie die zoekt in een string naar het eerst te vinden nummer en transformeert deze naar een nummer.
Er is ook parseFloat.
Gebruik dit alleen met string waardes.

```js
parseInt( 0.000008 );		// 0   ("0" from "0.000008")
parseInt( 0.0000008 );		// 8   ("8" from "8e-7")
parseInt( false, 16 );		// 250 ("fa" from "false")
parseInt( parseInt, 16 );	// 15  ("f" from "function..")

parseInt( "0x10" );			// 16
parseInt( "103", 2 );		// 2

*—> Boolean
Boolean( ) is een manier om een waarde in een boolean om te zetten.

var a = "0";
var b = [];
var c = {};

var d = "";
var e = 0;
var f = null;
var g;

Boolean( a ); // true
Boolean( b ); // true
Boolean( c ); // true

Boolean( d ); // false
Boolean( e ); // false
Boolean( f ); // false
Boolean( g ); // false

var a = "0";
var b = [];
var c = {};

var d = "";
var e = 0;
var f = null;
var g;

!!a;	// true
!!b;	// true
!!c;	// true

!!d;	// false
!!e;	// false
!!f;	// false
!!g;	// false
var b = a ? true : false;
```

Bovenstaande zou expliciet te noemen zijn, maar a moet eerst naar een boolean worden omgezet impliciet. Dit heet dus explicitly implicit.

### Implicit Coercion

Dit zijn type conversies, die niet duidelijk zijn, voor jou als developer.
Het doel hiervan: verminderen van breedsprakigheid, standaardtekst, en / of onnodige implementatie details, die de code opvullen met rommel.

### Strings <—> Numbers

Als een van de twee operands een string is, wordt het bij + een string, anders zal het een nummer worden.

```js
42 + “” // “42”
```

### Booleans —> Numbers

```js
function onlyOne() {
	var sum = 0;
	for (var i=0; i < arguments.length; i++) {
		// skip falsy values. same as treating
		// them as 0's, but avoids NaN's.
		if (arguments[i]) {
			sum += arguments[i];
		}
	}
	return sum == 1;
}

var a = true;
var b = false;

onlyOne( b, a );        // true
onlyOne( b, a, b, b, b );    // true

onlyOne( b, b );        // false
onlyOne( b, a, b, b, b, a );    // false
```

### Alles —> Boolean

Dingen die impliciet iets naar een boolean omvormen:

* If statement
* For (second clause)
* While en do while
* Ternary operator
* && || -> Moeten eigenlijk operand selector operators worden genoemd, omdat het niet duidelijk is wat ze doen

Guard operator: De eerste expressie test beschermt de tweede expressie:

```js
function foo() {
    console.log( a );
}

var a = 42;

a && foo(); // 42
```

Als _a_ niet truthy is, zal foo nooit worden aangeroepen, dit heet *short circuiting*.
De impliciete transformatie naar een boolean zal plaatsvinden nadat de compound expression is geëvalueerd.

### Symbol Coercion

Expliciete coercion naar strings is toegestaan, maar impliciet niet en geeft een error.
Ook kan het nooit naar een nummer gecoerced worden, maar wel naar een boolean (dat wordt true).

### Loose equals vs. Strict equals

*==* : Sta coercion toe in de vergelijking.
*===* : Sta geen coercion toe in de vergelijking.

### Abstract equality

*==* heet eigenlijk de abstract equality comparison algorithm.

+0 en -0 zijn gelijk aan elkaar.
Objecten (ook functies en arrays) zijn alleen gelijk aan elkaar als ze beide een referentie hebben met exact dezelfde waarde. Hier gebeurt geen coercion.
== en === gedragen zich precies hetzelfde als je objecten met elkaar vergelijkt.

#### Comparing: strings to number

Strings worden omgezet naar nummers.

#### Comparing: anything to boolean

Booleans worden omgezet naar nummers en vervolgens vergeleken.

```js
var x = true;
var y = "42";

x == y; // false
```

Een boolean wordt altijd eerst omgezet in een nummer, als het wordt vergeleken.

```js
var a = "42";

// bad (will fail!):
if (a == true) {
	// ..
}

// also bad (will fail!):
if (a === true) {
	// ..
}

// good enough (works implicitly):
if (a) {
	// ..
}

// better (works explicitly):
if (!!a) {
	// ..
}

// also great (works explicitly):
if (Boolean( a )) {
	// ..
}

```

#### Comparing: null to undefined

Als je null en undefined met == vergelijkt, zal dit altijd true geven.

#### Comparing: object to non-objects

In deze situatie worden objecten omgezet met toPrimitive en vervolgens vergeleken.
In een array worden nummers omgezet in strings en dan als er vergeleken wordt met == omgezet tot nummers.

```js
var a = "abc";
var b = Object( a );	// same as `new String( a )`

a === b;				// false
a == b;					// true
```

Gevallen waar dit niet zo is:

```js
var a = null;
var b = Object( a );	// same as `Object()`
a == b;					// false

var c = undefined;
var d = Object( c );	// same as `Object()`
c == d;					// false

var e = NaN;
var f = Object( e );	// same as `new Number( e )`
e == f;					// false
```

### Edge cases

```js
"0" == null;			// false
"0" == undefined;		// false
"0" == false;			// true -- UH OH!
"0" == NaN;				// false
"0" == 0;				// true
"0" == "";				// false

false == null;			// false
false == undefined;		// false
false == NaN;			// false
false == 0;				// true -- UH OH!
false == "";			// true -- UH OH!
false == [];			// true -- UH OH!
false == {};			// false

"" == null;				// false
"" == undefined;		// false
"" == NaN;				// false
"" == 0;				// true -- UH OH!
"" == [];				// true -- UH OH!
"" == {};				// false

0 == null;				// false
0 == undefined;			// false
0 == NaN;				// false
0 == [];				// true -- UH OH!
0 == {};				// false

0 == "\n";		// true
```

Het laatste voorbeeld hierboven werkt, omdat ieder karakter met een soort van witruimte wordt via toNumber omgezet naar 0.

Je moet loose equal vergelijkingen met false altijd vermijden.

### Safely using implicit coercion

Je moet ervoor zorgen dat je van te voren weet welke waardes er aan beide kanten van een vergelijking komen te staan.

Om problemen te voorkomen gebruik de volgende stappen:

1. Als een van de kanten true of false kan hebben, gebruik dan nooit ==.
2. Als een van de kanten [], “” of 0 kan hebben, vraag je af of je == wilt gebruiken.

Een andere plek waar je coercion kunt gebruiken, zonder angst, is met de typeof operator.
Deze geeft één van de zeven strings terug, genoemd in H1, hiervan is er geen één een “”.

[Javascript Equality Table](https://github.com/dorey/JavaScript-Equality-Table)

### Abstract relational comparison

Dit algorithme wordt altijd afgehandeld met <.
Dus a > b, wordt afgehandeld als b < a.

Dit algorithme roept eerst toPrimitive aan op beide waardes, als één van de twee resultaten daarvan geen string is, worden beide waardes omgezet naar nummers.

```js
var a = { b: 42 };
var b = { b: 43 };

a < b;	// false
```

Dit wordt false, omdat beide variabelen omgezet worden tot [object Object], waardoor ze gelijk zijn aan elkaar en dus niet minder.

<= wordt in JS vaak gezien als not greater than.

## You don't know JS - Types & Grammar - H5

**Grammar**: Hoe de JS taal syntax werkt. Het beschrijft de regels over hoe een taal werkt.

**Expression** en **statement** zijn niet hetzelfde.
Statements zijn volledige zinnen en expressions zijn delen van zinnen, regels. Operators zijn de samenvoegingen tussen regels.

Een statement bevat expressions.
Als je een waarde ergens aan toewijst, heet dat een **declaration statement**.
A = 3 * 6 is een voorbeeld van een **assignment expression**. Deze zijn altijd zonder het var keyword.
Als je alleen een expressie hebt, heet dat een **expression statement**.

Je krijgt undefined bij het verklaren van een variabele in de console, omdat het zo in de spec staat.

**REPL**: Read, evaluate, print, loop tool.

### Statement completion values

De completion value van een statement is bijna als een impliciete return van het laatste statement waarde in het block. Om dit op een normale manier wel op te kunnen vangen, kun je:

* Eval gebruiken (doe dit niet).
* ES7 do expression.

```js
var a, b;

a = do {
	if (true) {
		b = 4 + 38;
	}
};

a;	// 42
```

Hier voert do een block uit (met een of meerdere statements erin) en de laatste statement completion value van de do expression kan aan een variabele worden toegewezen.

### Expression side effects

De meeste statements hebben geen onverwachte side effects.
Vaak hebben functie calls wel mogelijke bijeffecten.

```js
var a = 42;
var b = a++;

a;	// 43
b;	// 42
```

++ en - - kunnen beide worden gebruikt als **postfix** (na) en **prefix** (voor).
Als het in de prefix versie wordt gebruikt, gebeurt het side effect voordat de waarde is gereturned.
Het side effect verdwijnt niet als je het in ( ) wrapt.

, = **Statement-series comma operator**.

```js
var a = 42, b;
b = ( a++, a );

a;	// 43
b;	// 43
```

Dit betekent: de tweede expressie (a) zal worden uitgevoerd, nadat het after side effect van a++ is gebeurt.

**delete** wordt gebruikt om properties van objecten te halen.
Het resultaat van het succesvol verwijderen van iets, is true als het lukt en false als het niet lukt.
Het side effect hiervan is, dat het een property verwijderd.

Van een assignment statement is het directe resultaat dat de waarde die eraan toe wordt gewezen, wordt gelogd en het neven effect is dat het ook echt wordt toegewezen.

```js
Var a, b, c;
A = b = c = 42;
```

C = 42 wordt eerst uitgevoerd, gevolgd door b = 42, gevolgd door a = 42.
Let op dat je niet var a = b = c = 42 doet, want dat kan niet.

### Contextual rules

```js
Var a = {
	foo: bar( )
};
```

Hier is a een **l-value**, omdat het het eindpunt is van de assignment.
De curly braces is de **r-value**.

```js
{
	foo: bar( )
} // Dit is een standalone block.
```

Het is valide JS. En foo: bar( ) is een **labeled statement**. Dit is een soort van **goto**, wat volgens vele een hele slechte manier van coden is.
JS heeft **labeled jumps**. Het betekent niet letterlijk ga hierheen, maar meer dat het hier iets mee moet doen.

```js
// `foo` labeled-loop
foo: for (var i=0; i<4; i++) {
	for (var j=0; j<4; j++) {
		if ((i * j) >= 3) {
			console.log( "stopping!", i, j );
			// break out of the `foo` labeled loop
			break foo;
		}

		console.log( i, j );
	}
}
// 0 0
// 0 1
// 0 2
// 0 3
// 1 0
// 1 1
// 1 2
// stopping! 1 3
```

Statement labels kunnen geen quotes om zich heen hebben, zoals dat bij JSON wel zo is.
**JSON-P**: Het wrappen van JSON data in een functie. Het zorgt er voor dat JSON valide JS syntax wordt.

### Blocks

```js
[] + {}; // "[object Object]"
{} + []; // 0
```

### Object Destructuring

Een andere plek waar je {} tegenkomt is bij een destructuring assignment.

```js
function getData() {
	// ..
	return {
		a: 42,
		b: "foo"
	};
}

var { a, b } = getData();

console.log( a, b ); // 42 “foo"
```

Het kan ook gebruikt worden voor het direct deconstructen van objecten als parameters in functies:

```js
function foo({ a, b, c }) {
	// no need for:
	// var a = obj.a, b = obj.b, c = obj.c
	console.log( a, b, c );
}

foo( {
	c: [1,2,3],
	a: 42,
	b: "foo"
} );	// 42 "foo" [1, 2, 3]
```

### Else if and optional blocks

In JS is er geen else if, maar doordat je met een if en else de {} kan omzeilen, wordt else if geldige syntax. Under the hood wordt het omgezet tot slechts if else chains genest.

### Operator precedence

De , operator heeft de laagste presedence.
Het chainen van verschillende operators achter elkaar is iets wat heel vaak gebeurd.
&& heeft de hoogste presedence, gevolgt door ||.

### Short circuited

Dit betekent en komt voor als een van de twee operatoren (&& of ||) de linker operand als genoege neemt om de uitkomt van de operation te weergeven.

### Tighter binding

De ternary operator heeft minder precedence dan de && of ||. De laatste twee *binden dus hechter*.

Operators zijn óf **links-associatief** of **rechts-associatief**. Dit slaat op de manier of groeperen wordt toegepast op basis van links naar rechts.
&& is links-associatief, net als ||.
Rechts associativiteit heeft niks te maken met rechts-naar-links evaluatie van de code. Het betekent het groeperen van rechts naar links.

De ternary operator is rechts-associatief.

```js
true ? false : true ? true : true;		// false

true ? false : (true ? true : true);	// false
(true ? false : true) ? true : true;	// true
```

Ook de = operator is rechts-associatief.

```js
var a, b, c;

a = b = c = 42;
```

### Disambiguation

Je moet beide operator presedence en handmatig groeperen ( ) in je programma’s mixen. Gebruik handmatig groeperen als je verwarring moet verminderen en duidelijkheid moet scheppen.

### Automatic semicolons

**ASI**: Automatic Semicolon Insertion. Dit betekent het vervangen van vergeten semicolons op plekken waar het wel nodig is.
Dit gebeurt, omdat als je één semicolon zou vergeten en het dit niet zou doen, je hele programma zou falen.
ASI gebeurt alleen als er sprake is van een *newline*.

ASI komt ook voor:

* Na do … while (a)
* Break
* Continue
* Return -> Als je multiline wilt returnen, moet je het wrappen in ( ).
* ES6 yield

### Error correction

Bijna alle semicolons zijn optioneel, behalve die in de for.
ASI is een **error correction routine**, met als error **parser error**.
Gebruik gewoon zo veel mogelijk wel semicolons, waar ze nodig zijn.

### Errors

**Early errors**: Errors die gebeuren tijdens het compilen, hieronder vallen ook grammatische fouten.
Doordat ze niet gevonden kunnen worden in het executen van je code, kan je ze niet catchen.

Early errors:

* Invalide regular expressions.
* Waardes aan de linker kant van een assignment operation.
* Duplicate functie parameter namen.
* Object literal met twee keer dezelfde naam.

Technisch gezien zijn dit niet echt syntax errors, maar meer **grammar errors**, maar omdat dat type error niet bestaat, wordt een **SyntaxError** teruggegeven.

### Using variables too early

ES6 heeft een nieuw concept mogelijk gemaakt: **TDZ** (Temporal Dead Zone).
Dit slaat op een plek in de code, waar de variabele referentie nog niet gemaakt kan worden, omdat het nog niet zijn vereiste initialisatie heeft bereikt.

Het duidelijkste voorbeeld komt uit ES6 let block-scoping:

```js
{
	a = 2;		// ReferenceError!
	let a;
}
```

Er zit een duidelijk verschil in een variabele die helemaal niet in een block is verklaard en een variabele die wel verklaard is, maar nog niet tot de initialisatie is gekomen. (**undefined vs ReferenceError**).

### Function arguments

Je kan ook de TDZ fout krijgen, als je in een functie in de default parameters een variabele van buiten aan een parameter assignt.

```js
function foo( a = 42, b = a + 1 ) {
	console.log( a, b );
}

foo();					// 42 43
foo( undefined );		// 42 43
foo( 5 );				// 5 6
foo( void 0, 7 );		// 42 7
foo( null );			// null 1
```

Null wordt omgezet in het cijfer 0 als je null + 1 doet.
Bij een **default parameter** in ES6 is er geen onderscheid tussen undefined en het niet meegeven van een waarde aan die parameter.
Je kan wel zien of er een undefined wordt meegegeven door te checken via arguments[waarde waar je undefined zou verwachten].

```js
function foo(a) {
	a = 42;
	console.log( arguments[0] );
}

foo( 2 );	// 42 (linked)
foo();		// undefined (not linked)
```

In het voorbeeld hierboven zijn de meegegeven arguments slot (arguments[x]) en de benaamde parameter gelinkt aan dezelfde waarde. In strict mode werkt dit echter ook niet.

### try…finally

De code in het finally block zal altijd lopen, zelfs als er een error is. Het wordt altijd na try en catch gebruikt. Het lijkt op een callback functie, die altijd aangeroepen wordt.

```js
function foo() {
	try {
		return 42;
	}
	finally {
		console.log( "Hello" );
	}

	console.log( "never runs" );
}

console.log( foo() );
// Hello
// 42

function foo() {
	try {
		return 42;
	}
	finally {
		throw "Oops!";
	}

	console.log( "never runs" );
}

console.log( foo() );
// Uncaught Exception: Oops!
```

**Yield** kan worden gezien als een directe return statement. Echter, niet zoals een return, is een yield niet compleet totdat de generator is hervat. Finally zal niet direct na een try block lopen, met daarin een yield.

Als er een return is gezet in een finally block, zal deze de return van een try overschrijven. Je moet hiervoor wel expliciet return aanroepen.

### Switch

Als er in een switch een case matcht, zal dit block beginnen executen, totdat het een break tegenkomt of het eind van het switch block.

```js
var a = "42";

switch (true) {
	case a == 10:
		console.log( "10 or '10'" );
		break;
	case a == 42:
		console.log( "42 or '42'" );
		break;
	default:
		// never gets here
}
// 42 or ’42'
```

In dit geval moet bijvoorbeeld a == 10 gelijk zijn aan true.

```js
var a = "hello world";
var b = 10;

switch (true) {
	case (a || b == 10):
		// never gets here
		break;
	default:
		console.log( "Oops" );
}
// Oops
```

Als je wilt dat het bovenstaande voorbeeld werkt moet je (a || b == 10) expliciet naar een boolean omzetten door er !! Voor te zetten.

```js
switch (a) {
	case 1:
	case 2:
		// never gets here
	default:
		console.log( "default" );
	case 3:
		console.log( "3" );
		break;
	case 4:
		console.log( "4" );
}
// default
// 3
```

In dit geval kijkt de switch eerst of er een match is (die is er niet), vervolgens gaat deze terug naar de top en komt een default en een break (in case 3) tegen die die allebei uitvoert.

## You don't know JS - Scopes & Closures - Hoofdstuk 2

**Scope**: Een set regels, die leidend zijn voor hoe de Engine verschillende variabelen kan opzoeken met hun naam. Deze kan dan gevonden worden in de huidige scope, of in de geneste scopes waar deze call vandaan komt.

Twee manieren om met scopes om te gaan:

* Lexical Scope - Wordt het meest gebruikt.
* Dynamic Scope.

### Lex-time

De eerste stap in een traditionele fase van een standaard taal compiler, heet **lexing**.

**Lexical scope** is een scope die wordt gezet tijdens het lexing. Het wordt bepaald door de manier waarop jij je code schrijft en is eigenlijk altijd vast als het lexing bereikt.

```js
function foo(a) {

	var b = a * 2;

	function bar(c) {
		console.log( a, b, c );
	}

	bar(b * 3);
}

foo( 2 ); // 2 4 12
```

In dit voorbeeld zitten drie scopes, globale scope, foo’s inner scope met de waarde a meegenomen, en bar’s inner scope met de waarde c meegenomen. Deze scopes kunnen worden gezien als scope bubbles.

Deze bubbles zijn bepaald, door waar de scope blocks zijn geschreven.
Elke functie maakt een nieuwe bubble van scope.

### Look-ups

Als er twee variabelen met dezelfde naam binnen het bereik van de look-up zitten, pakt het altijd de dichtstbijzijnde. Als dezelfde naam op meerdere levels voorkomt, heet dat shadowing.

Globale variabelen zijn ook automatisch properties van het globale object, dus het is mogelijk om waardes niet alleen te refereren met hun lexicale naam, maar ook indirect als property van het globale object.

Het maakt niet uit waar je de functie vandaan aanroept of hoe, de lexicale scope is alleen bepaald door de plek waar deze is verklaard.

### Cheating lexical

Als je de lexicale scope faket, zal dit leiden tot veel slechtere performance.

**Eval**
Deze functie neemt een string als argument en behandeld vervolgens de content van de string alsof het geschreven is op dat moment in het programma.

```js
function foo(str, a) {
	eval( str ); // cheating!
	console.log( a, b );
}

var b = 2;

foo( "var b = 3;", 1 ); // 1 3
```

In dit geval zal er in foo een nieuwe variabele b worden aangemaakt, die de globale b overshadowt.

Als je in strict mode zit, zal eval in zijn eigen lexicale scope werken. In dit geval zullen veranderingen die in eval gedaan worden, niet de omringende scope van waar deze is aangeroepen, aanpassen.

Andere dingen in JS, die ongeveer hetzelfde doen:

* setInterval
* setTimeout
* Function constructor

**With**
Dit is een depricated kenmerk van JS.
With wordt normaal gezien als een short-hand voor het maken van meerdere property references tegen een object, zonder het object steeds opnieuw te refereren.

```js
var obj = {
	a: 1,
	b: 2,
	c: 3
};

// more "tedious" to repeat "obj"
obj.a = 2;
obj.b = 3;
obj.c = 4;

// "easier" short-hand
with (obj) {
	a = 3;
	b = 4;
	c = 5;
}
```

Het bovenstaande ziet er logisch uit, maar er gaat wel een hoop fout achter de schermen:

```js
function foo(obj) {
	with (obj) {
		a = 2;
	}
}

var o1 = {
	a: 3
};

var o2 = {
	b: 3
};

foo( o1 );
console.log( o1.a ); // 2

foo( o2 );
console.log( o2.a ); // undefined
console.log( a ); // 2 -- Oops, leaked global!
```

With maakt een hele nieuwe lexicale scope uit het niets.
Doordat er geen variabele a in het tweede object zit dat meegegeven werd, wordt er een globale variabele a aangemaakt.
Deze functie is in strict mode niet meer toegestaan.

### Performance

Als de engine with of eval tegenkomt, moet deze gaan gokken, of al de locaties van de variabelen wel correct zijn.
Dit zorgt ervoor dat de engine helemaal geen performance optimalizations meer doet.

Gebruik deze twee manieren niet.

## You don't know JS - Scopes & Closures - Hoofdstuk 3

### Scope from functions

Een functie is een manier om een scope te maken. Dingen die in deze scope zijn gedefineerd zijn daarbuiten niet beschikbaar. Met dit patroon maak je goed gebruik van de dynamische aard van JS variabelen.

### Hiding in plain scope

Je kan code verstoppen door een functie eromheen te zetten.

Waarom je dit zou doen komt voort uit **Principles of Least Privilege**, ofwel **Least Authority**, of **Least Exposure**. De reden: verstop alles, behalve dat wat nodig is om je API werkend te krijgen voor mensen die het gebruiken.

Het vrijgeven van variabelen, die bij een functie horen, aan (vaak) de globale scope, is niet alleen onnodig, maar ook gevaarlijk, omdat ze zomaar eens veranderd zouden kunnen worden.

### Collision avoidance

Een ander voordeel van het verstoppen van variabelen en functies, is dat je voorkomt dat je per ongeluk variabele namen overwrite.

### Global namespaces

Als je veel verschillende libraries in je JS laadt, die niet hun variabelen goed zouden verstoppen, zou dat veel overwriting en errors veroorzaken.Goede libraries gebruiken vaak een unieke naam en wordt vervolgens gebruikt als namespace voor die library.

### Module management

Een andere mogelijkheid om collision te vermijden is het gebruiken van de moderne module techniek. Met deze techniek wordt deze code in een privé, onmogelijk te botsen scope gezet.

### Functions as scopes

Het hebben van functies als scopes is vaak niet ideaal, omdat je ze moet aanroepen en een naam moet geven, maar je kan wel gebruik maken van een **IIFE**.

Als function het eerste woord is in een statement heet het een function declaration en anders een function expression.

In een IIFE is de naam van de functie niet buiten de omringende ( ) beschikbaar.

### Anonymous vs. named

```js
setTimeout( function(){
	console.log("I waited 1 second!");
}, 1000 );
```

Het bovenstaande is een anonieme functie expressie. Functie expressies kunnen anoniem zijn, maar functie declarations niet.

Nadelen aan anonieme functies:

* Debugging moeilijker.
* Als je in de functie naar deze functie moet refereren, moet je de deprecated arguments.callee gebruiken.
* Verminderd leesbaarheid.

Inline function expressions zijn krachtig en bruikbaar, het maakt niet uit of ze benaamd zijn of niet. Gebruik altijd een naam in je function expressions.

### Invoking function expressions immediately

Immediately Invoked Function Expression: IIFE. Gebruik ook hier gewoon een naam.

(function { } ( )) is hetzelfde als (function { })( )

Je kan ook parameters meegeven aan een IIFE.

Met een IIFE kan je ook heel goed ervoor zorgen dat in die scope undefined niet veranderd is.

Een ander gebruik van een IIFE is om de volgorde van dingen te veranderen, met het UMD (Universal Module Definition) project:

```js
var a = 2;

(function IIFE( def ){
	def( window );
})(function def( global ){

	var a = 3;
	console.log( a ); // 3
	console.log( global.a ); // 2

});
```

Hier is de dev function scope gegeven in het tweede deel van de snippet.

### Blocks as scopes

**Block scoping** gaat over het verklaren van variabelen zo dichtbij en lokaal mogelijk als waar ze gebruikt moeten gaan worden.
Block scoping is een tool om Principles of Least Exposure te verlengen.

Block scoping bestaat niet direct in JS.
Sommige kenmerken van JS doen daar wel op lijken:
 With
 Try / Catch -> Het catch deel is geblockscoped.
 Let -> Koppelt een variabele aan de scope van een block code ({ }) waar deze in is geplaatst. Sommige mensen plaatsen liever om alles waar ze een block van willen maken { } dit is dan een expliciete manier van scoping. Anders is het impliciet.  Verklaringen die met let zijn gedaan zullen niet hoisten, dus als je ze probeert te bereiken voordat ze gedefineerd zijn, krijg je een referenceerror.

### Garbage collection

Een andere reden waarom block-scoping handig is, heeft te maken met closures en garbage collection om geheugen terug te winnen.

```js
function process(data) {
	// do something interesting
}

// anything declared inside this block can go away after!
{
	let someReallyBigData = { .. };

	process( someReallyBigData );
}

var btn = document.getElementById( "my_button" );

btn.addEventListener( "click", function click(evt){
	console.log("button clicked");
}, /*capturingPhase=*/false );
```

### Let loops

Als je gebruik maakt van let loops zal de variabele die je daarin aanmaakt niet buiten de loop beschikbaar zijn.

Let bindt i aan de for loop body en herbind het iedere iteratie van de loop.
Let bindt zich aan artibraire blocks code in plaats van functie scopes of globale scopes, kunnen er problemen opspelen als je de code gaat refactoren.

### Const

Dit maakt ook een block scoped variabele, maar die waarde kan niet worden veranderd.

## You don't know JS - Scopes & Closures - Hoofdstuk 4 - Hoisting

Iedere variabele verklaard in een scope is verbonden met die scope.

### Chicken or the egg?

Je JS programma wordt uitgevoerd van **top-to-bottom**, echter is er één ding dat fout denken over je programma kan opleveren.

```js
a = 2;

var a;

console.log( a ); // 2

//////////////////////

console.log( a );

var a = 2; // undefined
```

Wat komt er eerder, de kip (assignment) of het ei (declaration)?

### The compiler strikes again

Alle verklaringen, van variabelen en functies, zullen als eerst worden uitgevoerd in je code.

Var a = 2 lijkt alsof het één statement is, maar het wordt door de compiler opgedeeld in twee delen: var a en a = 2.

Het eerste deel van de statement (declaration) wordt verwerkt tijdens de compilation phase, terwijl het tweede deel van de statement (assignment) wordt op zijn plaats gelaten tot de execution phase.

Het tweede voorbeeld is dus eigenlijk:

```js
console.log( a );

a = 2;
```

Vandaar dat er een undefined wordt gegeven.

Variabele en functie verklaringen (var a) worden naar het bovenste deel van de code in de huidige scope geplaatst, vandaar de naam hoisting.
De declaration komt dus eerder dan de assignment.

Hoisting gebeurt dus per scope.

**Function declarations** worden gehoist, maar **function expressions** niet.

```js
foo(); // not ReferenceError, but TypeError!

var foo = function bar() {
	// ...
};
```

In dit geval wordt foo losgehaald van de expression en boven de executing declaration gezet, waardoor er een functie call gedaan wordt op undefined en dat levert een TypeError op.

### Functions first

Functions worden als eerst gehoist, gevolgd door de variabelen.

```js
foo(); // 1

var foo;

function foo() {
	console.log( 1 );
}

foo = function() {
	console.log( 2 );
};

//////////////////////////

function foo() {
	console.log( 1 );
}

foo(); // 1

foo = function() {
	console.log( 2 );
};
```

Doordat in dit geval in de bovenste code var foo een duplicate was, werd deze genegeerd, zelfs terwijl het voor de functie verklaring kwam. Dit werkt, omdat functies dus hoger in de rangorde staan als het om hoisting gaat.

Als je echter meer functies on elkaar hebt met dezelfde naam, dan zal deze echter wel de eerste variant overschrijden.

```js
foo(); // "b"

var a = true;
if (a) {
   function foo() { console.log( "a" ); }
}
else {
   function foo() { console.log( "b" ); }
}
```

Je kan beter functies in blocks vermijden.

## You don't know JS - Scopes & Closures - Hoofdstuk 4 - Scope Closures

**Closures** zijn overal in JS en je moet ze kunnen herkennen en er mee om gaan.
Closures zijn een resultaat van het schrijven van code, dat vertrouwt op de **lexical scope**.

### Nitty Gritty
Een closure betekent: Het herinneren en toegang hebben tot de lexicale scope van een functie, terwijl die functie wordt uitgevoerd buiten diens lexical scope.

De lookup rules van de lexical scope zijn slecht een (belangrijk) deel van closure, maar het is niet het enige.

Als iets over de scope van een ander iets ‘closes’ dan heeft het eerste iets een closure over de scope van het andere iets.

```js
function foo() {
	var a = 2;

	function bar() {
		console.log( a );
	}

	return bar;
}

var baz = foo();

baz(); // 2 -- Whoa, closure was just observed, man.
```

In dit geval wordt bar aangeroepen buiten de lexical scope, waar hij in is verklaard, omdat je het als waarde meegeeft aan de baz variabele.

Omdat bar nog een referentie heeft naar de scope, nadat het is uitgevoerd (omdat het via een variabele is meegegeven) zal deze niet worden garbage collected. Deze referentie is een closure.

Closure zorgt ervoor dat functies toegang behouden tot de lexicale scope, zoals deze was bepaald tijdens author-time.

Iedere manier waarop inner functions meegegeven worden aan een scope buiten hun eigen lexical scope, zal de binnenste functie toegang houden tot de originele waardes van de lexicale scope en zal de closure blijven bestaan.

Een **IIFE** wordt niet uitgevoerd buiten zijn lexicale scope, waardoor er vaak geen closure zichtbaar is.

### Loops + Closure

```js
for (var i=1; i<=5; i++) {
	setTimeout( function timer(){
		console.log( i );
	}, i*1000 );
}
```

In dit geval wordt ‘6’ vijf keer uitgeprint in de console. Dit komt omdat de ‘uitvoerende condition’ van de loop is, wanneer i niet minder is dan of gelijk aan 5. De eerste keer dat dat het geval is, is als i ‘6’ is.

Alle functies in de for loop worden wel apart aangemaakt, maar ze hebben allemaal closure over de gedeelde globale scope, die slechts één i in zich heeft.

In dit geval heb je een nieuwe closure nodig voor iedere iteratie van de loop.

Als je hier een lege IIFE omheen zet, werkt het alsnog niet, omdat het dan iedere keer alsnog dezelfde i pakt, echter als je var j = i boven de setTimeout in deze functie zet, werkt het wel.

### Block Scoping Revisited
In het bovenstaande voorbeeld had je een per-iteration block scope nodig om het op te lossen.

Let veranderd als het ware een block in een scope waar we closure over hebben. Om die reden werkt de volgende code wel, ten opzichte van de vorige bovenstaande gevallen:

```js
for (var i=1; i<=5; i++) {
	let j = i; // yay, block-scope for closure!
	setTimeout( function timer(){
		console.log( j );
	}, j*1000 );
}
```

Het kan zelfs nog makkelijk worden gemaakt met JS, doordat er speciaal gedrag is vastgesteld voor let in het hoofd van een for-loop. Als je hier namelijk let gebruikt, zal dit aangeven dat je de variabele niet slechts één keer wilt verklaren voor de hele loop, maar voor iedere iteratie.

```js
for (let i=1; i<=5; i++) {
	setTimeout( function timer(){
		console.log( i );
	}, i*1000 );
}
```

### Modules
Er zijn nog meer code patronen, die de kracht van closures omarmen, maar aan het oppervlak geen schijn van callbacks tonen, hiervan is de meest bekende en krachtigste het module patroon. De meest bekende vorm binnen het module pattern is de revealing module.

```js
function CoolModule() {
	var something = "cool";
	var another = [1, 2, 3];

	function doSomething() {
		console.log( something );
	}

	function doAnother() {
		console.log( another.join( " ! " ) );
	}

	return {
		doSomething: doSomething,
		doAnother: doAnother
	};
}

var foo = CoolModule();

foo.doSomething(); // cool
foo.doAnother(); // 1 ! 2 ! 3
```

De bovenstaande CoolModule( ) is slechts een functie, die moet worden aangeroepen, zodat er een module instance wordt gemaakt.

Hetgeen wat hierboven wordt gereturnt kan worden gezien als de public API van de module, aangezien deze gereturnde waardes geen toegang geven tot de privé variabelen.

De innerlijke functies hebben closure over de binnenste scope van de instance van de module, doordat deze wordt aangeroepen en dus ergens anders beschikbaar worden.

Vereisten module pattern:
Er moet een omringende functie zijn, die wordt aangeroepen, ten minste één keer.
De omringende functie moet tenminste één binnenste functie returnen, zodat deze functie closure heeft over de privé scope en toegang heeft tot en/of de privé state kan aanpassen.

De bovenstaande code maakt het niet uit hoeveel module instanties ervan afstammen. Als een module daar wel om geeft heet het een singleton.

```js
var foo = (function CoolModule() {
	var something = "cool";
	var another = [1, 2, 3];

	function doSomething() {
		console.log( something );
	}

	function doAnother() {
		console.log( another.join( " ! " ) );
	}

	return {
		doSomething: doSomething,
		doAnother: doAnother
	};
})();

foo.doSomething(); // cool
foo.doAnother(); // 1 ! 2 ! 3
```

In het bovenstaande geval is de module omgezet tot IIFE, die direct wordt uitgevoerd en aan een variabele wordt meegegeven.

Modules zijn functies, dus ze kunnen parameters meekrijgen.

Een andere krachtige, kleine, variatie op een singleton is door een benoemd object te returnen met de naam publicAPI.

```js
var foo = (function CoolModule(id) {
	function change() {
		// modifying the public API
		publicAPI.identify = identify2;
	}

	function identify1() {
		console.log( id );
	}

	function identify2() {
		console.log( id.toUpperCase() );
	}

	var publicAPI = {
		change: change,
		identify: identify1
	};

	return publicAPI;
})( "foo module" );

foo.identify(); // foo module
foo.change();
foo.identify(); // FOO MODULE
```

Doordat hier een referentie tot de public API wordt behouden kun je van die instance, van binnen uit dingen veranderen, zoals het toevoegen of verwijderen van methodes, properties en diens waardes.

### Modern Modules
Veel dependency loaders/managers verpakken dit module verklaringspatroon in een vriendelijke API. Het werkt als volgt:

```js
var MyModules = (function Manager() {
	var modules = {};

	function define(name, deps, impl) {
		for (var i=0; i<deps.length; i++) {
			deps[i] = modules[deps[i]];
		}
		modules[name] = impl.apply( impl, deps );
	}

	function get(name) {
		return modules[name];
	}

	return {
		define: define,
		get: get
	};
})();
```

In het bovenstaande geval is dit belangrijk:

```js
modules[name] = impl.apply(impl, deps)
```

Dit voert de functie (die meegegeven wordt) uit, met de dependencies als parameter(s). Vervolgens wordt de gereturnde waarde opgeslagen (de API van die module) in een interne lijst van modules die worden gevolgd per naam.

Vervolgens kunnen er dingen mee gedaan worden op de volgende manier:

```js
MyModules.define( "bar", [], function(){
	function hello(who) {
		return "Let me introduce: " + who;
	}

	return {
		hello: hello
	};
} );

MyModules.define( "foo", ["bar"], function(bar){
	var hungry = "hippo";

	function awesome() {
		console.log( bar.hello( hungry ).toUpperCase() );
	}

	return {
		awesome: awesome
	};
} );

var bar = MyModules.get( "bar" );
var foo = MyModules.get( "foo" );

console.log(
	bar.hello( "hippo" )
); // Let me introduce: hippo

foo.awesome(); // LET ME INTRODUCE: HIPPO
```

### Future Modules
Met de nieuwe ES6 module syntax, kan je je JS opdelen in files en al deze losse files worden als modules behandeld. Iedere module kan dingen importeren, net als exporteren.

**Statically recognized pattern**: Iets waar de compiler iets van begrijpt.

**ES6 Module API’s** zijn statisch (de API’s veranderen niet tijdens het uitvoeren van de code). Aangezien de compiler dat weet, kan en zal deze tijdens het compilen kijken of de referentie naar de gemaakte geïmporteerde module API ook echt bestaat.

ES6 modules hebben geen inline variant, dus als je ze wilt gebruiken moet je ze allemaal los in aparte files zetten. Doordat de browsers een module loader hebben, zullen de files geïmporteerd worden in de volgorde waarop ze zijn aangegeven.

import x from “y” haalt een deel van een module op, terwijl module x from “x” de hele api van die module ophaalt.

De inhoudt van een module file wordt behandeld, alsof er een omringende scope closure omheen ligt, zoals at bij functie-closure modules ook zo is.

## You don't know JS - This & Object Prototypes - Hoofdstuk 1 - This or That?

**This**: Een speciaal identifier keyword, dat automatisch wordt bepaald in de scope van iedere functie.

### Why this?

```js
function identify() {
	return this.name.toUpperCase();
}

function speak() {
	var greeting = "Hello, I'm " + identify.call( this );
	console.log( greeting );
}

var me = {
	name: "Kyle"
};

var you = {
	name: "Reader"
};

identify.call( me ); // KYLE
identify.call( you ); // READER

speak.call( me ); // Hello, I'm KYLE
speak.call( you ); // Hello, I'm READER
```

Zonder `this`:

```js
function identify(context) {
	return context.name.toUpperCase();
}

function speak(context) {
	var greeting = "Hello, I'm " + identify( context );
	console.log( greeting );
}

identify( you ); // READER
speak( me ); // Hello, I'm KYLE
```

This zorgt voor een elegantere manier van het doorgeven van referenties naar objecten. Dit leidt weer tot een schonere API en het makkelijker hergebruiken van functies.

### Itself

This refereert niet naar de functie zelf.
Je kan **state** opslaan (als waardes in properties van een functie).

Veel developers vallen terug op een ander mechanisme als ze niet snappen waarom het onderstaande niet werkt, zoals ze willen.

```js
function foo(num) {
	console.log( "foo: " + num );

	// keep track of how many times `foo` is called
	this.count++;
}

foo.count = 0;

var i;

for (i=0; i<10; i++) {
	if (i > 5) {
		foo( i );
	}
}
// foo: 6
// foo: 7
// foo: 8
// foo: 9

// how many times was `foo` called?
console.log( foo.count ); // 0 -- WTF?
```

De oplossing is ook niet per se, om de naam van de functie te gebruiken als this (het kan wel, maar dan moet je functie wel altijd een naam hebben):

```js
function foo() {
	foo.count = 4; // `foo` refers to itself
}

setTimeout( function(){
	// anonymous function (no name), cannot
	// refer to itself
}, 10 );
```

Wat wel werkt, is .call() te gebruiken:

```js
function foo(num) {
	console.log( "foo: " + num );

	// keep track of how many times `foo` is called
	// Note: `this` IS actually `foo` now, based on
	// how `foo` is called (see below)
	this.count++;
}

foo.count = 0;

var i;

for (i=0; i<10; i++) {
	if (i > 5) {
		// using `call(..)`, we ensure the `this`
		// points at the function object (`foo`) itself
		foo.call( foo, i );
	}
}
// foo: 6
// foo: 7
// foo: 8
// foo: 9

// how many times was `foo` called?
console.log( foo.count ); // 4
```

### Its scope

Veel andere mensen denken dat `this` verwijst naar de scope van de functie. Dit is deels, maar niet volledig waar.

Het verwijst **niet** niet naar de **lexical scope** van de functie.

```js
function foo() {
	var a = 2;
	this.bar();
}

function bar() {
	console.log( this.a );
}

foo(); //undefined
```

In dit bovenstaande voorbeeld gaan meerdere dingen mis, ten eerste dat this.bar() wordt aangeroepen (wat overigens wel lukt), om vervolgens te falen bij het loggen van this.a.

Je kan this niet gebruiken om in de lexicale scope iets op te zoeken.

### What's this?

This heeft niks te maken met waar de functie is verklaard, maar juist de manier waarop deze wordt aangeroepen.

Als een functie wordt aangeroepen, wordt er een **activation record** of **execution context** aangemaakt. Deze bevat informatie over:

* **Waar** de functie **vandaan** is aangeroepen (**call-stack**)
* **Hoe** de functie is aangeroepen
* Welke parameters er werden meegegeven
* Etcetera

Hierin staat ook een waarde van de 'this' reference, die voor de levensduur van de functie geldt.

## You don't know JS - This & Object Prototypes - Hoofdstuk 2 - This all makes sense now!

This binding is volledig afhankelijk van de **call-site** (Hoe de functie is aangeroepen).

### Call-site

Dit is de locatie van waar de functie vandaan is aangeroepen,niet waar die functie verklaard is.

Het is belangrijk om over de **call-stack** (de functies die zijn aangeroepen tot op dit moment) na te denken.

De **call-site** staat in de invocation *voor* de huidig uitvoerende functie.

```js
function baz() {
    // call-stack is: `baz`
    // so, our call-site is in the global scope

    console.log( "baz" );
    bar(); // <-- call-site for `bar`
}

function bar() {
    // call-stack is: `baz` -> `bar`
    // so, our call-site is in `baz`

    console.log( "bar" );
    foo(); // <-- call-site for `foo`
}

function foo() {
    // call-stack is: `baz` -> `bar` -> `foo`
    // so, our call-site is in `bar`

    console.log( "foo" );
}

baz(); // <-- call-site for `baz`
```

Je kan de call-stack vinden via de debugger in de browser.

### Nothing but rules

#### Default binding

De standaard versie van this binding, komt van standaard alleenstaande functie calls. Dit is de default, als geen van de onderstaande regels gelden.

```js
function foo() {
	console.log( this.a );
}

var a = 2;

foo(); // 2
```

Als 'strict mode' aan staat breekt de bovenstaande code, omdat het globale object niet **default binding** ondersteunt.

```js
function foo() {
	"use strict";

	console.log( this.a );
}

var a = 2;

foo(); // TypeError: `this` is `undefined`
```

Dit geldt echter alleen als de content van de foo function 'strict mode' aan heeft staan, als de call-site dit aan heeft staan, refereert this wel naar het globale object.

Vaak kom je dit probleem niet tegen, want je hele code loopt óf in strict mode, of niet.

#### Implicit binding

Heeft de call-site een **context object** of **owning / containing object**.

```js
function foo() {
	console.log( this.a );
}

var obj = {
	a: 2,
	foo: foo
};

obj.foo(); // 2
```

Ookal heeft foo een reference in het object gekregen, wordt de functie niet eigendom of omringd door een object, zoals de regel doet denken.

In dit geval gebruikt de call-site de context van het object om te refereren naar de functie. In dit geval is het object eigenaar en omringer van de **functie referentie**.

Alleen het laatste / hoogste level van een object property reference chain geldt voor de call-site.

```js
function foo() {
	console.log( this.a );
}

var obj2 = {
	a: 42,
	foo: foo
};

var obj1 = {
	a: 2,
	obj2: obj2
};

obj1.obj2.foo(); // 42
```

#### Implicitly lost

Als een implicitly bound function de binding met **this** verliest, om vervolgens terug te vallen op **default binding**.

```js
function foo() {
	console.log( this.a );
}

var obj = {
	a: 2,
	foo: foo
};

var bar = obj.foo; // function reference/alias!

var a = "oops, global"; // `a` also property on global object

bar(); // "oops, global"
```

In dit geval is bar() de call site, wat dus **default binding** veroorzaakt en refereert naar het globale object.

Ook als je functies meegeeft via de parameters, geldt het bovenstaande fenomeen:

```js
function foo() {
	console.log( this.a );
}

function doFoo(fn) {
	// `fn` is just another reference to `foo`

	fn(); // <-- call-site!
}

var obj = {
	a: 2,
	foo: foo
};

var a = "oops, global"; // `a` also property on global object

doFoo( obj.foo ); // "oops, global"
```

Zelfs als de functie een ingebouwde JS functie is, zoals setTimeout(), geldt dit.

#### Explicit binding

Als je een function call wilt dwingen om een bepaald object te gebruiken als **this** binding, zonder een property reference op een object te zetten.

Enkele tools om dit te doen in JS zijn, dingen zoals **.call() en .apply()**. Elke functie die je zelf maakt heeft deze properties via diens prototype.

Deze functies werken, door beide als eerste argument een object mee te krijgen, die gebruikt moet worden voor this, om vervolgens de functie aan te roepen met die this.

```js
function foo() {
	console.log( this.a );
}

var obj = {
	a: 2
};

foo.call( obj ); // 2
```

Als je een string meegeeft als this, wordt deze gewrapt in diens Object vorm (new String etc.).

Als het om this binding gaat, gedragen beide methodes (call en apply) zich hetzelfde, behalve als er meerdere parameters worden meegegeven.

Dit zorgt er nog niet voor dat een functie diens bedoelde this binding verliest.

##### Hard binding

```js
function foo() {
	console.log( this.a );
}

var obj = {
	a: 2
};

var bar = function() {
	foo.call( obj );
};

bar(); // 2
setTimeout( bar, 100 ); // 2

// `bar` hard binds `foo`'s `this` to `obj`
// so that it cannot be overriden
bar.call( window ); // 2
```

Het type binding, dat hierboven wordt gebruikt, is beide **sterk en expliciet**, dus vandaar dat het **hard binding** heet.

Het maakt hierbij niet uit, hoe je de functie bar aanroept, foo zal altijd worden gebonden aan obj.

Door **arguments** te gebruiken kan je alsnog parameters meegeven aan de inner function.

```js
function foo(something) {
	console.log( this.a, something );
	return this.a + something;
}

var obj = {
	a: 2
};

var bar = function() {
	return foo.apply( obj, arguments );
};

var b = bar( 3 ); // 2 3
console.log( b ); // 5
```

Je kan ook een **bind helper** maken.

```js
function foo(something) {
	console.log( this.a, something );
	return this.a + something;
}

// simple `bind` helper
function bind(fn, obj) {
	return function() {
		return fn.apply( obj, arguments );
	};
}

var obj = {
	a: 2
};

var bar = bind( foo, obj );

var b = bar( 3 ); // 2 3
console.log( b ); // 5
```

Dit patroon is zo standaard geworden dat sinds ES5 er een ingebouwde functie in is gebouwd: **Function.prototype.bind**.

```js
function foo(something) {
	console.log( this.a, something );
	return this.a + something;
}

var obj = {
	a: 2
};

var bar = foo.bind( obj );

var b = bar( 3 ); // 2 3
console.log( b ); // 5
```

##### API Call 'Contexts'

Veel API's hebben een optionele parameter, met de **context** van this, zodat bind() niet gebruikt hoeft te worden.

```js
function foo(el) {
	console.log( el, this.id );
}

var obj = {
	id: "awesome"
};

// use `obj` as `this` for `foo(..)` calls
[1, 2, 3].forEach( foo, obj ); // 1 awesome  2 awesome  3 awesome
```

### new Binding

In class-oriented languages, zijn constructors speciale methodes op classes die die functie uitvoeren als de class wordt aangeroepen met **new**.

De JS syntax lijkt hetzelfde, maar het is achter de schermen totaal niet zo.

**constructors** zijn functies die worden aangeroepen met het new keyword voor zich.

Ze zijn niet verbonden aan classes, en ze vormen een class ook niet. Het zijn geen eens speciale functies.

Elke functie met **new** ervoor kan worden gezien als **constructor call**.

Als een functie wordt aangeroepen met new ervoor, dus een constructor call wordt gedaan, dan gebeuren de volgende dingen automatisch:
1. Een nieuw object wordt gemaakt.
2. Het nieuwe object wordt via prototype gelinkt.
3. Het nieuwe object wordt gezet als **this** voor die functie call.
4. Tenzij de functie een alternatief object returnt, zal de new-aangeroepen functie automatisch het nieuwe object returnen.

```js
function foo(a) {
	this.a = a;
}

var bar = new foo( 2 );
console.log( bar.a ); // 2
```

### Everything in order

Als meerdere van de bovenstaande regels gelden voor function binding, heeft **default binding** altijd de laagste prioriteit.

```js
function foo() {
	console.log( this.a );
}

var obj1 = {
	a: 2,
	foo: foo
};

var obj2 = {
	a: 3,
	foo: foo
};

obj1.foo(); // 2
obj2.foo(); // 3

obj1.foo.call( obj2 ); // 3
obj2.foo.call( obj1 ); // 2
```

Zoals hier te zien is, heeft **explicit binding** meer voorang dan **implicit binding**.

```js
function foo(something) {
	this.a = something;
}

var obj1 = {
	foo: foo
};

var obj2 = {};

obj1.foo( 2 );
console.log( obj1.a ); // 2

obj1.foo.call( obj2, 3 );
console.log( obj2.a ); // 3

var bar = new obj1.foo( 4 );
console.log( obj1.a ); // 2
console.log( bar.a ); // 4
```

Zoals hier te zien heeft **new binding** meer voorang dan **implicit binding**.

new en call/apply zijn niet te combineren. Je kan wel **hard binding** gebruiken.

**new binding** heeft meer voorang dan en zal dus **hard binding** overriden.

Dit kan, omdat het handig kan zijn om hard binding te overriden:
> The primary reason for this behavior is to create a function (that can be used with new for constructing objects) that essentially ignores the this hard binding but which presets some or all of the function's arguments. One of the capabilities of bind(..) is that any arguments passed after the first this binding argument are defaulted as standard arguments to the underlying function (technically called "partial application", which is a subset of "currying").

```js
function foo(p1,p2) {
	this.val = p1 + p2;
}

// using `null` here because we don't care about
// the `this` hard-binding in this scenario, and
// it will be overridden by the `new` call anyway!
var bar = foo.bind( null, "p1" );

var baz = new bar( "p2" );

baz.val; // p1p2
```

### Determining this

1. Als de functie met new wordt aangeroepen, is `this` het nieuw gemaakte object.
2. Als de functie aangeroepen wordt met call, apply of bind dan is `this` het meegegeven object.
3. Als de functie met een context wordt aangeroepen, is `this` die context.
4. Anders in strict mode undefined of de global object.

### Binding exceptions

#### Ignored this

Als je null of undefined mee geeft aan een expliciete binding, zijn die waardes genegeerd en zal de default binding het overnemen.

**Apply** kan worden gebruikt om arrays van waardes te spreaden in een functie call.
**Bind** kan parameters **curryen** (standaard waardes zetten).

```js
function foo(a,b) {
	console.log( "a:" + a + ", b:" + b );
}

// spreading out array as parameters
foo.apply( null, [2, 3] ); // a:2, b:3

// currying with `bind(..)`
var bar = foo.bind( null, 2 );
bar( 3 ); // a:2, b:3
```

Er zit echter een gevaar in het altijd gebruiken van undefined of null bij deze methodes, omdat als je het doet bij een library waar je geen controle over hebt, er wellicht 'per ongeluk' veranderingen aan het globale object worden gedaan.

#### Safer this

Het opzetten van objecten, voor `this`, zodat het geen problematische side-effects heeft voor je programma heet **DMZ** (De-Militarized Zone).

Om dit te doen kan je dus gewoon een leeg object meegeven aan de bind functies. De beste manier om een heel leeg object te maken is met Object.create(null), omdat Object.prototype hier niet op zit.

#### Indirection

Je kan ook *indirecte referenties* maken naar functies, bewust of niet, en in die gevallen zullen de **default binding** regels worden toegepast.

#### Softening binding

**Hard-binding** verminderd de flexibiliteit van een functie aanzienlijk.
**Soft-binding** een manier om alternatief gedrag te stellen voor **default binding**, terwijl het mogelijk blijft om `this bound` te kunnen worden, via impliciete of expliciete bindings.

```js
function foo() {
   console.log("name: " + this.name);
}

var obj = { name: "obj" },
    obj2 = { name: "obj2" },
    obj3 = { name: "obj3" };

var fooOBJ = foo.softBind( obj );

fooOBJ(); // name: obj

obj2.foo = foo.softBind(obj);
obj2.foo(); // name: obj2   <---- look!!!

fooOBJ.call( obj3 ); // name: obj3   <---- look!

setTimeout( obj2.foo, 10 ); // name: obj   <---- falls back to soft-binding
```

#### Lexical this

ES6 introduceert een nieuw soort functie, die niet de bovenstaande vier regels volgt: **arrow functions**.

`=>` **fat-arrow operator**

Arrow functions nemen `this` over van de enclosing scope (function of global).

```js
function foo() {
	// return an arrow function
	return (a) => {
		// `this` here is lexically adopted from `foo()`
		console.log( this.a );
	};
}

var obj1 = {
	a: 2
};

var obj2 = {
	a: 3
};

var bar = foo.call( obj1 );
bar.call( obj2 ); // 2, not 3!
```

In dit geval is foo bound aan obj1. bar zal dan ook this-bound zijn aan obj1, deze kan niet worden overschreven, zoals te zien is bij de laatste call, zelfs niet met new.

## You don't know JS - This & Object Prototypes - Hoofdstuk 3 - Objects

**Objects** komen in twee vormen:

* **Declarative of literal form**
* **Constructed form**

```js
// Literal
var myObj = {
	key: value
	// ...
};

// Constructed
var myObj = new Object();
myObj.key = value;
```

Je gebruikt bijna altijd de literal form.

### Type

Objects zijn een van de zes primaire JS types.
Dingen, zoals string, number, boolean, null en undefined zijn zelf geen objecten.

Er zijn enkele **complex primitives**:

* Functions - Sub-type van een object - **callable object**.
* Arrays - Sub-type van een object - Meer gestructureerd dan normale objecten.

### Built-in objects

Er zijn nog meer sub-types van objecten (**built-in objects**):

* String
* Number
* Boolean
* Object
* Function
* Array
* Date
* RegExp
* Error

Deze staan niet gelijk aan hun primitieve waardes.
Dit zijn eigenlijk allemaal ingebouwde functies, in JS.

```js
var strPrimitive = "I am a string";
typeof strPrimitive;							// "string"
strPrimitive instanceof String;					// false

var strObject = new String( "I am a string" );
typeof strObject; 								// "object"
strObject instanceof String;					// true

// inspect the object sub-type
Object.prototype.toString.call( strObject );	// [object String]
```

Om dingen met de waarde te doen van bijvoorbeeld een string moet het naar een String object vorm worden omgezet, gelukkig gebeurt dat automatisch, dus hoef je bijna nooit de constructed vorm te gebruiken.

null en undefined hebben geen object wrapper vorm, alleen de primitieve waardes.

Date kan alleen worden aangemaakt met de constructed vorm.

Gebruik alleen de constructed vorm als je extra opties nodig hebt.

### Contents

De content van objecten bestaan uit waardes, die worden opgeslagen op specifieke benaamde locaties, die **properties** heten.

De waardes van een property hoeven niet altijd in het object zelf aanwezig te zijn.

Om properties te bereiken in een object gebruik je:

* **.** operator / property access - Heeft een Identifier toegankelijke naam nodig.
* **[ ]** operator / key access - Kan elke UTF-8 / Unicode string bereiken.

Je kan met de key access operator programmatisch de identifier opbouwen:

```js
var wantA = true;
var myObject = {
	a: 2
};

var idx;

if (wantA) {
	idx = "a";
}

// later

console.log( myObject[idx] ); // 2
```

Alle property namen worden naar strings omgezet.

### Computed property names

ES6 voegt **computed property names** toe:

```js
var prefix = "foo";

var myObject = {
	[prefix + "bar"]: "hello",
	[prefix + "baz"]: "world"
};

myObject["foobar"]; // hello
myObject["foobaz"]; // world
```

Dit type wordt vooral gebruikt in ES6 Symbols.

### Property vs. method

Functies die tot een object behoren worden gezien als **methods**, in andere talen.

In JS wordt een property niet een **method** als het toevallig de waarde van een functie heeft.

**Function** en **method** zijn te verwisselen als benaming voor een functie.

### Arrays

Arrays worden ook bereikt met de key access methode.
Arrays slaan waardes op, op basis van **numeric indexing**. Dit betekent dat de waardes worden opgeslagen in locaties, die vaak **indices** worden genoemd.

Je kan ook properties toevoegen op arrays, dit veranderd niet de length van een array.

Als je een property toevoegd op een array, en het kan worden omgezet worden tot / is een nummer, dan wordt deze waarde toegevoegd aan de array.

### Duplicating objects

Er is geen ingebouwde manier om objecten te kopiëren in andere objecten.

Er zit verschil tussen **shallow copy** en **deep copy** van objecten. Een deep copy zorgt voor circulation en een shallow copy zou alleen waardes kopiëren.

Een manier om objecten te kopiëren is via **JSON.parse**, als een object naar een JSON string kan worden omgezet en vervolgens met dezelfde structuur en waardes kan worden omgezet tot object.

Je kan het beste een shallow copy maken, in ES6 zit nu Object.assign() voor deze taak. Deze neemt een *target object* als eerste parameter en een of meerdere *source objects* als de rest parameters.

Deze zal over alle **enumerable**, **owned keys** (die direct aanwezig zijn), van de source objects loopen en die kopieëren via '=' naar het *target object*, het returnt vervolgs het *target object*.

```js
var newObj = Object.assign( {}, myObject );

newObj.a;						// 2
newObj.b === anotherObject;		// true
newObj.c === anotherArray;		// true
newObj.d === anotherFunction;	// true
```

### Property descriptors

Sinds ES5 zijn alle properties beschreven in termen van een  **property descriptors**.

```js
var myObject = {
	a: 2
};

Object.getOwnPropertyDescriptor( myObject, "a" );
// {
//    value: 2,
//    writable: true,
//    enumerable: true,
//    configurable: true
// }
```

Als een property descriptor alleen maar data waardes heeft heet het een **data descriptor**.

Als een object **configurable** is, dan kan je via de **Object.defineProperty()** methode bestaande properties aanpassen, en als het **writable** is, kun je hier dingen aan toevoegen.

```js
var myObject = {};

Object.defineProperty( myObject, "a", {
	value: 2,
	writable: true,
	configurable: true,
	enumerable: true
} );

myObject.a; // 2
```

#### Writable

Als je een object via de defineProperty methode op writable: false zet, dan kan je die property niet meer veranderen.
Je krijgt een TypeError in strict mode.

#### Configurable

Als je een configurable property via de bovenstaande methode op false zet kan je die niet meer terug zetten naar true, het levert een TypeError op.

Als een property al configurable false is, kan je writeable nog wel naar false zetten, maar niet meer naar true.

**configurable:false** zorgt er ook voor dat je een property niet meer kan verwijderen met **delete**.

#### Enumerable

Deze karakteristiek beheert of een property te vinden is in **object-property enumerations**, zoals een **for..in** loop. Je kan alsnog de waardes bereiken, op alle andere manieren.

#### Immutability

Soms wil je properties hebben, die niet kunnen worden veranderd, sinds ES5 kan dat. Alle mogelijkheden om dit te doen, zorgen voor **shallow immutability**, dit betekent dat het alleen het object en de directe properties omvat. Als je diepere elementen, zoals arrays ook immutable wilt hebben, zul je het volgende proces voor die ook moeten herhalen.

##### Object constant

Als je *writable: false* en *configurable:false* combineert, creëer je als het ware een **constant** (iets dat niet kan worden verwijderd, veranderd of hergedefineerd).

```js
var myObject = {};

Object.defineProperty( myObject, "FAVORITE_NUMBER", {
	value: 42,
	writable: false,
	configurable: false
} );
```

##### Prevent extensions

Als je wilt dat een object geen *nieuwe* properties kan krijgen, maar degene die die al heeft onveranderd laat kun je **Object.preventExtensions()** aanroepen.

```js
var myObject = {
	a: 2
};

Object.preventExtensions( myObject );

myObject.b = 3;
myObject.b; // undefined
```

##### Seal

**Object.seal()** maakt een sealed object, wat betekent het pakt een bestaand object en roept daarop aan Object.preventExtensions(), maar zet ook diens configurable: false.

Je kan dus geen properties meer toevoegen, maar je kan ook de bestaande properties niet meer veranderen of verwijderen. Je kan nog wel de waardes veranderen.

##### Freeze

**Object.freeze()** doet hetzelfde als seal, maar zet ook alle **data accesor** properties writable: false, zodat de waardes niet meer kunnen veranderen.

Dit is de hoogst mogelijke vorm van immutability.

### [[Get]]

```js
var myObject = {
	a: 2
};

myObject.a; // 2
```

Volgens de specificatie voort de bovenstaande code een **[[Get]] operation** uit.

Deze methode bekijkt eerst of het object een property heeft met de naam die wordt opgevraagd, als dat niet zo is zal de [[Prototype]] chain worden gevolgd.

Als het via de bovenstaande manier, op geen enkele manier, een waarde kan teruggeven voor de gewenste property, zal undefined worden teruggegeven.

### [[Put]]

Je zou denken dat deze methode wordt aangeroepen als je een waarde toevoegd aan een object, maar het ligt meer genuanceerd, voornamelijk met betrekking tot het gedrag dat gebeurt als het property al bestaat.

1. Is de property een **accesor descriptor**? Roep dan de setter aan, als die er is.
2. Is de property een **data descriptor** met writable:false, doe niks in non-strict, en geef een TypeError in strict mode.
3. Zet anders de waarde als normaal.

### Getters & Setters

ES5 zorgt ervoor dat je de standaard acties van de [[Set]] en [[Put]] methodes deels kan overschrijven, per property.

**Getters** zijn properties die een verborgen functie aanroepen, om een waarde te verkrijgen.

**Setters** zijn properties die een verborgen functie aanroepen, om een waarde te setten.

Als een property opzet, zodat deze een getter of setter, of beide heeft, wordt deze een **accessor descriptor**.

```js
var myObject = {
	// define a getter for `a`
	get a() {
		return 2;
	}
};

Object.defineProperty(
	myObject,	// target
	"b",		// property name
	{			// descriptor
		// define a getter for `b`
		get: function(){ return this.a * 2 },

		// make sure `b` shows up as an object property
		enumerable: true
	}
);

myObject.a; // 2

myObject.b; // 4
```

Dit zijn twee manieren om een getter te maken.

```js
var myObject = {
	// define a getter for `a`
	get a() {
		return 2;
	}
};

myObject.a = 3;

myObject.a; // 2
```

In dit geval is alleen een getter gemaakt, en wordt bij een poging om de waarde van a te veranderen deze assignment genegeerd.

```js
	// define a getter for `a`
	get a() {
		return this._a_;
	},

	// define a setter for `a`
	set a(val) {
		this._a_ = val * 2;
	}
};

myObject.a = 2;

myObject.a; // 4
```

Om dit wel mogelijk te maken, moet je altijd een setter defineren.

### Existence

```js
var myObject = {
	a: 2
};

("a" in myObject);				// true
("b" in myObject);				// false

myObject.hasOwnProperty( "a" );	// true
myObject.hasOwnProperty( "b" );	// false
```

Je kan een van deze twee manieren gebruiken, om erachter te komen of een property bestaat op een object, of dat er gewoon undefined aan deze property is toegewezen.

De **in** methode kijkt of het object een property heeft met die naam, of dat het in de prototype zit.
De **hasOwnProperty** methode kijkt alleen of het object een property heeft met die naam. Deze kijkt ook naar de [[Prototype]]

### Enumeration

Niet enumerable properties worden alsnog gezien via hasOwnProperty en de in methode, behalve als de in methode zich bevindt in een for loop.
**Object.keys(obj)** returnt een array van alle enumerable properties.
**Object.getOwnPropertyNames(obj)** returnt een array van alle properties, of ze enumerable of niet zijn maar niet uit.

Deze twee methodes kijken niet naar de [[Prototype]].

### Iteration

Als je wilt itereren over de waardes van een object, wordt bij indexed-arrays vaak een for-loop gebruikt, dit is echter niet itereren over de waardes, maar over de **indices**.

**forEach()** itereert over alle waardes in een array en negeert iedere callback return waardes.
**every()** blijft itereren, totdat het einde van de array is bereikt, of de callback een falsy value returnt.
**some()** blijft itereren, totdat het einde van de array is bereikt, of de callback een truthy value returnt.

Als je direct over de waardes van een array, of object properties wilt itereren, kun je de ES6 **for..of** loop gebruiken.

Deze werkt als volgt:

```js
var myArray = [ 1, 2, 3 ];
var it = myArray[Symbol.iterator]();

it.next(); // { value:1, done:false }
it.next(); // { value:2, done:false }
it.next(); // { value:3, done:false }
it.next(); // { done:true }
```

Waarom je hier Symbol gebruikt: het houdt een speciale naamwaarde, niet een speciale waarde.

Je moet één keer meer it.next() aanroepen, om de done's naar true te zetten.

Gewone objecten hebben geen **@@iterator**. Deze kan je er wel handmatig op zetten.

```js
var myObject = {
	a: 2,
	b: 3
};

Object.defineProperty( myObject, Symbol.iterator, {
	enumerable: false,
	writable: false,
	configurable: true,
	value: function() {
		var o = this;
		var idx = 0;
		var ks = Object.keys( o );
		return {
			next: function() {
				return {
					value: o[ks[idx++]],
					done: (idx > ks.length)
				};
			}
		};
	}
} );

// iterate `myObject` manually
var it = myObject[Symbol.iterator]();
it.next(); // { value:2, done:false }
it.next(); // { value:3, done:false }
it.next(); // { value:undefined, done:true }

// iterate `myObject` with `for..of`
for (var v of myObject) {
	console.log( v );
}
// 2
// 3
```



## You don't know JS - This & Object Prototypes - Hoofdstuk 4 -


## You don't know JS - This & Object Prototypes - Hoofdstuk 5 -
