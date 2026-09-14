# Šablóna záverečnej práce

## Informácie o projekte

- **Autor:** Ing. Tomáš Bača
- **Fakulta:** Fakulta riadenia a informatiky, Žilinská univerzita v Žiline
- **Verzia:** 1.0
- **Licencia:** MIT License (pozri súbor `LICENSE`)

Hlavný zdrojový súbor LaTeX pre záverečnú prácu. Kompilácia prebieha pomocou **LuaLaTeX**, text je sadzovaný písmom **Source Serif 4** a matematická časť písmom **Cambria Math**. Bibliografia je spracovaná nástrojom **Biber**.

---

# Návod na použitie

## Požiadavky

- Kompilátor: **LuaLaTeX**
- Bibliografický systém: **Biber**

Odporúčaný editor:

- **TeXStudio**: https://www.texstudio.org

---

## Inštalácia Perl

Na správnu funkciu nástroja **Biber** je potrebné mať nainštalovaný **Perl**.

Inštalačné balíky:

- https://www.perl.org/get.html

### Windows

Odporúčaná distribúcia:

- Strawberry Perl

### Linux a macOS

Distribúcia Perl býva štandardne súčasťou operačného systému.

---

## Inštalácia LaTeX distribúcie

LaTeX distribúcia poskytuje:

- kompilátory,
- balíky,
- správu závislostí,
- nástroje na vytváranie dokumentov.

Odporúčaná distribúcia:

- **MiKTeX**: https://miktex.org

Počas inštalácie nastavte:

```text
Install missing packages on-the-fly = Yes
```

---

## Nastavenie TeXStudio

Prejdite do Options → Configure TeXstudio

V nastaveniach aktivujte:

```text
Show Advanced Options
```

Potom prejdite do:

```text
Build → Meta Commands → Build & View
```

a nastavte:

```text
txs:///lualatex |
txs:///biber |
txs:///makeglossaries |
txs:///lualatex |
txs:///lualatex |
txs:///view
```

Potom prejdite do:

```text
Build → Meta Commands → Default Compiler
```

a nastavte:

```text
LuaLaTex
```

Potom prejdite do:

```text
Build → Meta Commands → Default Viewer
```

a nastavte:

```text
PDF Viewer
```

Potom prejdite do:

```text
Build → Meta Commands → Default Bibliography Tool
```

a nastavte:

```text
Biber
```

---

# Konfigurácia práce

## Základné informácie

Súbor:

```text
hlavicky/00_globalne_informacie_o_dokumente.tex
```

Obsahuje:

- údaje na titulnej strane,
- údaje na hlavičkách strán,
- údaje na hlavičkách abstraktov.

---

## Zadanie práce

Nahrajte PDF súbor:

```text
zadanie_prace/zadanie_prace.pdf
```

---

## Skratky, symboly a pojmy

### Skratky

```text
hlavicky/00_skratky_defincie.tex
```

### Symboly

```text
hlavicky/00_symboly_definicie.tex
```

### Pojmy

```text
hlavicky/00_pojmy_definicie.tex
```

---

## Čestné vyhlásenie, poďakovanie a abstrakty

Súbor:

```text
hlavicky/00_informacie_cestne_vyhlasenie_podakovanie_abstrakt.tex
```

Obsahuje:

- čestné vyhlásenie,
- poďakovanie,
- abstrakt v slovenčine,
- abstrakt v angličtine,
- kľúčové slová.

Text sa automaticky prenesie na príslušné strany.

---

## Kapitoly práce

Všeobecné informácie k písaniu práce:

```text
kapitoly/jadro.tex
kapitoly/spracovanie_zaverecnej_prace.tex
```

---

# Bibliografia

Bibliografické zdroje ukladajte do:

```text
bibliografia/zaverecna_praca.bib
```

---

## Odporúčaný nástroj pre správu bibliografie

### JabRef

https://www.jabref.org/#download

Odporúča sa spustiť:

```text
Quality → Check Integrity
```

V `.bib` súbore by sa mali nachádzať iba upozornenia:

- `Journal not found in abbreviation list`
- `Citation key deviates from generated key`

---

## Formátovanie .bib súboru

Odporúčaný nástroj:

[https://flamingtempura.github.io/bibtex-tidy/](https://flamingtempura.github.io/bibtex-tidy/index.html?opt=%7B%22modify%22%3Atrue%2C%22omit%22%3A%5B%22abstract%22%5D%2C%22curly%22%3Atrue%2C%22numeric%22%3Atrue%2C%22months%22%3Atrue%2C%22space%22%3A2%2C%22tab%22%3Afalse%2C%22align%22%3A13%2C%22blankLines%22%3Atrue%2C%22duplicates%22%3A%5B%22key%22%2C%22doi%22%5D%2C%22stripEnclosingBraces%22%3Afalse%2C%22dropAllCaps%22%3Afalse%2C%22escape%22%3A%22new%22%2C%22unescape%22%3Afalse%2C%22sortFields%22%3A%5B%22title%22%2C%22shorttitle%22%2C%22author%22%2C%22year%22%2C%22month%22%2C%22day%22%2C%22journal%22%2C%22booktitle%22%2C%22location%22%2C%22on%22%2C%22publisher%22%2C%22address%22%2C%22series%22%2C%22volume%22%2C%22number%22%2C%22pages%22%2C%22doi%22%2C%22isbn%22%2C%22issn%22%2C%22url%22%2C%22urldate%22%2C%22copyright%22%2C%22category%22%2C%22note%22%2C%22metadata%22%5D%2C%22stripComments%22%3Atrue%2C%22trailingCommas%22%3Atrue%2C%22encodeUrls%22%3Atrue%2C%22tidyComments%22%3Atrue%2C%22removeEmptyFields%22%3Afalse%2C%22removeDuplicateFields%22%3Atrue%2C%22lowercase%22%3Atrue%2C%22backup%22%3Atrue%7D)

Nástroj automaticky:

- zoradí polia,
- odstráni duplicity,
- zjednotí formátovanie,
- zakóduje URL adresy,
- upraví odsadenie.

---

# Riešenie problémov

V prípade problémov s kompiláciou:

1. Skontrolujte súbor `.bib`.
2. Odstráňte problematické znaky.
3. Odstráňte HTML značky alebo neplatný obsah.

Medzi často problematické reťazce patria:

```text
<a
</a>
href=
target=
rel=
class=
data-lexical
_

&
#
``
$
#:~:text=

<script
<div
<span
<strong
<i>
</i>
<b>
</b>
```

Tieto znaky a značky môžu spôsobovať problémy pri kompilácii pomocou LuaLaTeX.

# Šablóna v angličtine 

https://github.com/tomasbaca438/LaTeX_final_thesis_template
