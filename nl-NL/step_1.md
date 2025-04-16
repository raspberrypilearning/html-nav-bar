### Voeg de HTML toe om de navigatiebalk weer te geven

De navigatiebalk wordt tussen de `<nav>`-tags in de header van de webpagina geplaatst.

Zoek de tags `<header>` en `</header>`.

Voeg de `<nav>`-tags toe.

## --- code ---

language: html
filename: index.html
line_numbers: true
line_number_start: 10
line_highlights: 11, 13
------------------------------------------------------------

```
<header>
  <nav>
    
  </nav>
</header>
```

\--- /code ---

Gebruik `<div>` om de links naar de andere pagina's op te nemen.

Voeg binnen de `<nav>`-tags een nieuwe `<div>` toe.

## --- code ---

language: html
filename: index.html
line_numbers: true
line_number_start: 10
line_highlights: 12-14
-----------------------------------------------------------

```
<header>
  <nav>
    <div>

    </div>
  </nav>
</header>
```

\--- /code ---

Voeg `<a>` tags toe om links naar elke pagina te maken.

## --- code ---

language: html
filename: index.html
line_numbers: true
line_number_start: 10
line_highlights: 13-15
-----------------------------------------------------------

```
<header>
  <nav>
    <div>
      <a href="index.html">Home</a>
      <a href="wildlife.html">Wilde dieren</a>
      <a href="climate.html">Klimaat</a>
    </div>
  </nav>
</header>
```

\--- /code ---

Voeg een `nav-items`-klassekenmerk toe aan de `<div>` die de navigatiebalklinks bevat.

## --- code ---

language: html
filename: index.html
line_numbers: true
line_number_start: 10
line_highlights: 12
--------------------------------------------------------

```
<header>
  <nav>
    <div class="nav-items">
      <a href="index.html">Home</a>
      <a href="wildlife.html">Wilde dieren</a>
      <a href="climate.html">Klimaat</a>
    </div>
  </nav>
</header>
```

\--- /code ---

### De hele navigatiebalk vormgeven

Open het bestand `style.css` en een `nav`-elementselector.

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 36
line_highlights:
-----------------------------------------------------

/\* Navigatiebalk \*/
nav {
padding: 0 15px;
height: 60px;
font-size: 22px;
display: flex;
justify-content: center;
align-items: center;
background-color: #33658A;
}

\--- /code ---

Maak een selector voor de klasse `nav-items` om de ruimte tussen de links te verdelen.

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 49
line_highlights: 50-53
-----------------------------------------------------------

/\* Navigatie-items \*/
.nav-items {
display: flex;
gap: 100px;
}

\--- /code ---

### De links opmaken

Je kunt niet alleen de hele navigatiebalk opmaken, maar ook afzonderlijke links.

Maak een andere selector om elke `<a>`-tag in de `nav-items`-div op te maken.

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 55
line_highlights: 56-60
-----------------------------------------------------------

/\* Navigatiebalklinks \*/
.nav-items > a {
color: #55DDE0;
text-decoration: none;
transition: .4s ease-in-out;
}

\--- /code ---

Voeg een selector toe om elke link op te maken wanneer je erover beweegt met je muis.

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 62
line_highlights: 63-65
-----------------------------------------------------------

/\* Muis over navigatielinks \*/
.nav-items > a:hover {
color: white;
}

\--- /code ---

### Een actieve link maken

De index.html pagina zal als eerste worden geladen.

Wanneer die pagina geopend is, moet de link wit blijven en niet aanklikbaar zijn.

Voeg een nieuwe `active` CSS class toe voor de link naar de pagina die momenteel geopend is.

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 67
line_highlights: 68-71
-----------------------------------------------------------

/\* Actieve navigatielinks\*/
.nav-items .active {
color: white;
pointer-events: none;
}

\--- /code ---

Open `index.html`.

Voeg het `active` klassekenmerk toe aan de index.html `<a>`-tag.

## --- code ---

language: html
filename: index.html
line_numbers: true
line_number_start: 10
line_highlights: 13
--------------------------------------------------------

```
<header>
  <nav>
    <div class="nav-items">
      <a href="index.html" class="active">Home</a>
      <a href="wildlife.html">Wilde dieren</a>
      <a href="climate.html">Klimaat</a>
    </div>
  </nav>
</header>
```

\--- /code ---
