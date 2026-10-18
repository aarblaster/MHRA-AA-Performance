# MHRA-AA-Performance

This is a modified version of the MHARA 4th Ed. CSL.
It is modified in the following way: It changes the 'film' category 
for citing live performance. 
It priorities dis-ambiguation in live performance by naming key 
creative participants.

## Usage
To use this CSL in Zotero, make sure that fields are entered in the
'extra' field for your records.

The full new field list is:
```
lighting-design: 
set-design: 
playwright:
choreographer:
composer:
conductor:
```

## Theatre

So for the production:
Title: The Woods
Playwright: Robert Allen-Evens
Director: Lucy Morrison
Set Designer: Naomi Dawson
Lighting Designer: Anthony Arblaster
Producer: Royal Court Theatre
Venue: Jerwood Theatre Upstairs, London
First Performance: 2018
Type: play

It maps the following fields
Director -> `director`
Playwright -> `playwright` **New**
Set Designer -> `set-design` **New**
Lighting Designer -> `lighting-design` **New**
Producer -> `distributor`
Type -> `genre`
Location -> `location`
Date -> `date`

This show would ouput as:
**Bibliography**
Morrison, Lucy (dir.), The Woods by Robert Allen-Evans, play, Naomie Dawson (set), Anthony Arblaster (ld.) (Royal Court Theatre, Jerwood Theatre Upstairs, London, 2018)


**Notes**
The Woods by Robert Allen-Evans, play, dir. by Lucy Morrison, set by Naomie Dawson, ld. by Anthony Arblaster (Royal Court Theatre, Jerwood Theatre Upstairs, London, 2018).

## Dance
Where the live performance is dance (contemporary or balet).
Omitting `director` and including `choreographer:` will ensure that the choreographer is listed first.
Choreographer will be abreviated to 'choreo.' thoughout.

For example:
Show: Romeo and Juliet
genre: dance
Choeographer: Mathew Bourne
set design: Lez Brotherston
lighting design: Paule Constable 
producers: New Adventures and Sadler’s Wells
Venue: Sadler’s Wells Theatre
City: London
first performance: 2019

This show will map to the following fields:
show --> `title`
genre --> `genre`
Choreographer --> `choreographer:` **New in extra**
Set Designer --> `set-design` **New**
Lighting Designer --> `lighting-design` **New**
Producer -> `distributor`
Venue and city --> `location`
first performance --> `date`


**Bibliography**
Bourne, Mathew (choreo.), Romeo and Juliet, dance, Lez Brotherston (set), Paule Constable (ld.) (New Adventures and Sadler’s Wells, Sadler’s Wells Theatre, London, 2019)


**Note**
Romeo and Juliet, dance, choreo. by Mathew Bourne, set by Lez Brotherston, ld. by Paule Constable (New Adventures and Sadler’s Wells, Sadler’s Wells Theatre, London, 2019).

## Opera
For Opera, simply imput all fields as if a play or muiscal, but avoid including a choreographer
as this will be included in the place of director.
For the composer enter as aditional text of `playwright:`. 