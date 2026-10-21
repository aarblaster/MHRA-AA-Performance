# MHRA-AA-Performance
![Static Badge](https://img.shields.io/badge/licence-CC%20BY%20SA-red)
![GitHub last commit](https://img.shields.io/github/last-commit/aarblaster/MHRA-AA-Performance)



This is a modified version of the MHARA 4th Ed. CSL.
It is modified in the following way: 
- It changes the 'film' category for citing live performance. 
- It priorities dis-ambiguation in live performance by naming key creative participants.
- It uses industry standard abreviations where possible (ld, dir, choreo)

## Author
This style is based on
[MHRA Style Guide 4th edition (notes)](https://github.com/citation-style-language/styles/blob/master/mhra-notes.csl)
by [Andrew Dunning](https://github.com/adunning), from the [Citation Style Language](https://citationstyles.org) project.

## Testing
This CSL style is only tested using [Zotero](https://zotero.org), and should be tested
before use in other citation tools.

## Usage
To use this CSL in Zotero, make sure that fields are entered in the
'extra' field for your records.

The full new field list is:
```
lighting-design: 
set-design: 
playwright:
choreographer:
choreographer-inverted:
conductor:
```

Enter each one on its own line at the top of 'extra', as `field: value`.
Names in these fields are printed exactly as you type them; Zotero cannot
reverse them (the `Surname || Forename` syntax only works for standard CSL
name fields such as `director`). That is why the choreographer has two fields:
see [Dance](#dance).

## Theatre

So for the production:
- Title: The Woods
- Playwright: Robert Allen-Evens
- Director: Lucy Morrison
- Set Designer: Naomi Dawson
- Lighting Designer: Anthony Arblaster
- Producer: Royal Court Theatre
- Venue: Jerwood Theatre Upstairs, London
- First Performance: 2018
- Type: play

It maps the following fields
- Director -> `director`
- Playwright -> `playwright` **New**
- Set Designer -> `set-design` **New**
- Lighting Designer -> `lighting-design` **New**
- Producer -> `distributor`
- Type -> `genre`
- Location -> `location`
- Date -> `date`

The `extra` field for this record reads:
```
playwright: Robert Alan Evens
set-design: Naomi Dawson
lighting-design: Anthony Arblaster
```

This show would ouput as:
**Bibliography**
Morrison, Lucy (dir.), The Woods by Robert Allen-Evans, play, Naomie Dawson (set), Anthony Arblaster (ld.) (Royal Court Theatre, Jerwood Theatre Upstairs, London, 2018)


**Notes**
The Woods by Robert Allen-Evans, play, dir. by Lucy Morrison, set by Naomie Dawson, ld. by Anthony Arblaster (Royal Court Theatre, Jerwood Theatre Upstairs, London, 2018).

## Dance
Where the live performance is dance (contemporary or ballet).
Omitting `director` and including `choreographer:` will ensure that the choreographer is listed first,
in the same place as a director.
Choreographer will be abbreviated to 'choreo.' throughout.

MHRA gives the name forename first in notes and surname first in the bibliography,
so enter the choreographer twice:
- `choreographer:` forename first, for notes (Matthew Bourne)
- `choreographer-inverted:` surname first, for the bibliography (Bourne, Matthew)

If `choreographer-inverted:` is missing, the bibliography falls back to the
forename-first name (Matthew Bourne (choreo.)).

For example:
- Show: Romeo and Juliet
- Genre: Dance
- Choreographer: Matthew Bourne
- Set Design: Lez Brotherston
- Lighting Design: Paule Constable 
- Producers: New Adventures and Sadler's Wells
- Venue: Sadler's Wells Theatre
- City: London
- First Performance: 2019

This show will map to the following fields:
- show --> `title`
- genre --> `genre`
- choreographer --> `choreographer:` and `choreographer-inverted:` **New in extra**
- Set Designer --> `set-design` **New in extra**
- Lighting Designer --> `lighting-design` **New in extra**
- Producer -> `distributor`
- Venue and city --> `location`
- first performance --> `date`


The 'extra' field for this record reads:
```
choreographer: Matthew Bourne
choreographer-inverted: Bourne, Matthew
set-design: Lez Brotherston
lighting-design: Paule Constable
```

**Bibliography**
Bourne, Matthew (choreo.), Romeo and Juliet, dance, Lez Brotherston (set), Paule Constable (ld.) (New Adventures and Sadler’s Wells, Sadler’s Wells Theatre, London, 2019)


**Note**
Romeo and Juliet, dance, choreo. by Matthew Bourne, set by Lez Brotherston, ld. by Paule Constable (New Adventures and Sadler’s Wells, Sadler’s Wells Theatre, London, 2019).

## Opera
For Opera, simply imput all fields as if a play or muiscal, but avoid including a choreographer
as this will be included in the place of director. 

For the composer enter as additional text of `playwright:`.
(`composer` is a standard CSL field, so filling it in would put the composer first,
in place of the director.)

## Licence
The original MHRA CSL style by [@adunning](https://github.com/adunning) and this adaptation 
is licensed under [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/). See [LICENSE](LICENSE).
