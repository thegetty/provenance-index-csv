# Goupil Stock Books DRAFT

### Table of Contents

* [License](#license)
* [Dataset description &amp; scope](#dataset-description--scope)
* [General editorial guidelines](#general-editorial-guidelines)
* [Data dictionary](#data-dictionary)

## License

The Goupil stock books dataset is offered under the Creative Commons [CC0 1.0 Universal Public Domain Dedication](https://creativecommons.org/publicdomain/zero/1.0/legalcode).

## Dataset Description & Scope

This dataset contains 43,750 records transcribed from the [15 stock books](http://hdl.handle.net/10020/900239_livre) of Goupil & Cie/Boussod, Valadon & Cie in Paris (1846-1919). [Read more about the Goupil stock books](http://www.getty.edu/research/tools/digital_collections/goupil_cie/index.html).

In general, stock books are administered by galleries and art dealers to record information about works of art that come into their inventories. Information from these stock books, of which the Goupil stock books are a prime example, includes the date of acquisition, dealer's costs, names of purchasers, date of sales, and selling prices for works of art bought and sold by the gallery. Most of the information provided is written in French, but some may be in English. Some handwritten notes may not be included. 

# Data Dictionary & Editorial Guidelines

## General editorial guidelines

Primarily, the dataset is a “verbatim” transcription of the stock books, meaning the editors transcribed exactly what was written in the source materials. However, as with many historical documents, there are inconsistencies and irregularities. To achieve a high level of accuracy
and clarity, editorial changes were made during and post-transcription:

-   Wherever possible, editors replaced shortcuts such as `do`, `idem`, 
    a hashmark (`#`), or double quote mark (`"`) with the actual word or
    name being referenced. 

-   Abbreviations may be spelled out.

-   Information in brackets was added by PSCP editors. The title ‘[sans titre]’ was added when a title could not be found. See     the ‘notes’ column below for more details about the use of brackets in specific fields. 

-   If `<br>` appears in the data, it indicates a link break. This
    may occur in any of fields with `alphabetic` in the `data_type`
    column below.

-   Names of artists, buyers, and sellers of a work are validated by an
    internal authority database, which is the source of authority
    names, nationalities, and locations. Most artists have been
    validated, but many buyers and sellers have yet to be fully
    researched so the corresponding authority fields may be empty.

-   Goupil recorded purchase, dealer’s cost, and sale prices using two alphabetic coding schemes. The main price codes and 
    their translations are included, but transaction details such as commission, restoration, framing, depreciation, etc., can      only be viewed using the [Stock Books](http://www.getty.edu/research/tools/digital_collections/goupil_cie/books.html).

The price coding schemes, which were handwritten by Dieterle on the title page of almost all of the stock books, are shown below:
for stock books 1-7:    A=1; M=2; O=3; N=4; S=5; I=6; E=7; U=8; R=9; X=0; Z=0 (“a monsieur”)
for stock books 8-15:  P=1; R=2; E=3; C=4; A=5; U=6; T=7; I=8; O=9; N=0; X=0; Z=0 Y=0 (“precaution”)


## Data dictionary


