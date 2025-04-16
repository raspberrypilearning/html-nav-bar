### Ajouter le code HTML pour afficher la barre de navigation

La barre de navigation est placée dans les balises `<nav>` de l'en-tête de la page web.

Trouve les balises `<header>` et `</header>`.

Ajoute les balises `<nav>`.

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

Utilise un `<div>` pour contenir les liens vers les autres pages.

À l'intérieur des balises `<nav>`, ajoute un nouveau `<div>`.

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

Ajoute des balises `<a>` pour créer des liens vers chaque page.

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
      <a href="index.html">Accueil</a>
      <a href="wildlife.html">Faune</a>
      <a href="climate.html">Climat</a>
    </div>
  </nav>
</header>
```

\--- /code ---

Ajoute un attribut de classe `nav-items` au `<div>` contenant les liens de la barre de navigation.

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
      <a href="index.html">Accueil</a>
      <a href="wildlife.html">Faune</a>
      <a href="climate.html">Climat</a>
    </div>
  </nav>
</header>
```

\--- /code ---

### Styliser toute la barre de navigation

Ouvre le fichier `style.css` et un sélecteur d'élément `nav`.

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 36
line_highlights:
-----------------------------------------------------

/\* Barre de navigation \*/
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

Crée un sélecteur pour la classe `nav-items` afin d'espacer les liens.

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 49
line_highlights: 50-53
-----------------------------------------------------------

/\* Élément de navigation \*/
.nav-items {
display: flex;
gap: 100px;
}

\--- /code ---

### Styliser les liens

En plus de styliser l'ensemble de la barre de navigation, tu peux styliser des liens individuels.

Crée un autre sélecteur pour styliser chaque balise `<a>` dans le div `nav-items`.

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 55
line_highlights: 56-60
-----------------------------------------------------------

/\* Liens de la barre de navigation \*/
.nav-items > a {
color: #55DDE0;
text-decoration: none;
transition: .4s ease-in-out;
}

\--- /code ---

Ajoute un sélecteur pour styliser chaque lien lorsque tu le survoles.

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 62
line_highlights: 63-65
-----------------------------------------------------------

/\* Survol des liens de navigation \*/
.nav-items > a:hover {
color: white;
}

\--- /code ---

### Créer un lien actif

La page index.html sera chargée en premier.

Lorsque cette page est ouverte, le lien doit rester blanc et ne pas être cliquable.

Ajoute une nouvelle classe CSS `active` pour le lien vers la page actuellement ouverte.

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 67
line_highlights: 68-71
-----------------------------------------------------------

/\* Liens actifs de navigation \*/
.nav-items .active {
color: white;
pointer-events: none;
}

\--- /code ---

Ouvre `index.html`.

Ajoute l'attribut de classe `active` à la balise `<a>` du fichier index.html.

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
      <a href="index.html" class="active">Accueil</a>
      <a href="wildlife.html">Faune</a>
      <a href="climate.html">Climat</a>
    </div>
  </nav>
</header>
```

\--- /code ---
