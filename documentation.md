# This is the documentation heading

## This is the chapter subheading

### Sub subheading

Dies ist ein normaler Textbereich  
in zwei Zeilen, da zwei Leerzeichen oder mehr einen Zeilenumbruch erzeugen.

Neuer Absatz

**Fettschrift**

[Referenzlink][1]

[1]:https://google.de

* Unsortierte Liste Item 1
* Unsortierte Liste Item 2
    * Unteritem 1
    * Unteritem 2
* Unsortierte Liste Item 3

1. Sortierte Liste Item 1
2. Sortierte Liste Item 2
3. Sortierte Liste Item 3







Margins, paddings, Breite, etc. immer in rem angeben.
Schriftgröße im html Selector sollte 10px ergeben, damit 1rem = 10px entspricht.  
Den Wert der html-Schriftgröße aber nicht in px, sondern in % (ausgehend von der Standard-Browserschriftgröße des Browsers (18px)) angeben.

Ordnerstruktur:

* root
    * resources
        * css
            * style.css
        * img
        * sass
            * abstracts
                * _functions.scss
                * _mixins.scss
                * _variables.scss
            * base
                * _animations.scss
                * _base.scss
                * _typography.scss
                * _utilities.scss
            * components
                * _button.scss
            * layout
                * _grid.scss
                * _header.scss
            * pages
                * _home.scss
            * main.scss
    * vendor
    * documentation.md
    * grid.html
    * index.html
    * package.json




Falls nicht geändert, ist Standardschriftgröße in Browsern 16px  
Mit folgendem SASS/SCSS kann man mithilfe von SASS-Funktionen einfach die gewünschte Pixelgröße angeben  
und es wird automatisch in em umgewandelt.  
  

**SCSS:**  

    $browser-context: 16;  //Default Browser Schriftgröße
  
    @function em($pixels, $context: $browser-context) {  
      @return #{$pixels/$context}em;  
    }

**SCSS-Anwendung:**

    .element-1 {
        font-size: em(32); //entspricht 32px
    }

    .element-2 {
        font-size: em(14); //entspricht 14px
    }

**CSS-Ergebnis:**

    .element-1 {
        font-size: 2em;
    }

    .element-2 {
        font-size: 0.875em;
    }

[Source](https://css-tricks.com/snippets/sass/px-to-em-functions/)  


## Resources

[Jonas Schmedtmann Resource page](https://codingheroes.io/resources)