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

-   The price coding schemes, which were handwritten by Dieterle on the title page of almost all of the stock books, are shown below:
    for stock books 1-7:    A=1; M=2; O=3; N=4; S=5; I=6; E=7; U=8; R=9; X=0; Z=0 (“a monsieur”)
for stock books 8-15:  P=1; R=2; E=3; C=4; A=5; U=6; T=7; I=8; O=9; N=0; X=0; Z=0 Y=0 (“precaution”)


## Data dictionary

|  **field_name** | **data_type** | **missing_values** | **field_description** | **field_example** | **internal_notes** | **public_notes** |
|  :------ | :------ | :------ | :------ | :------ | :------ | :------ |
|  pi_record_no | alphanumeric | n/a | Unique Getty-assigned number of 1 to 5 digits prefaced with "G-". | G-24567 |  |  |
|  **Multiple groups of stock book number fields, numbered sequentially from _1 to _15, may occur.** |  |  |  |  |  |  |
|  stock_book_no_1 | numeric | n/a | Number of the stock book in which the object appears. | 7 |  | See Goupil & Cie stock books |
|  stock_book_gno_1 | numeric | n/a | Stock number assigned by Goupil for the object. | 6944 |  |  |
|  stock_book_pg_1 | numeric | n/a | Page on which the record appears in the stock book. | 96 |  |  |
|  stock_book_row_1 | numeric | n/a | Row on the page where the record appears in the stock book. | 8 |  |  |
|  **Multiple groups of artist name fields, numbered sequentially from _1 to _2, may occur.** |  |  |  |  |  |  |
|  artist_name_1 | alphabetic | blank | Verbatim name of the first artist. | Van Schendel |  | Shortcuts such as "do" or "idem" are replaced by the actual name referenced. |
|  art_authority_1 | uppercase alphabetic | blank | Authority name for first artist, established by PSCP. | SCHENDEL, BERNARDUS VAN |  |  |
|  nationality_1 | alphabetic | blank | Authority for first artist's nationality, established by PSCP. | Dutch |  |  |
|  attribution_mod1 | alphabetic | blank | Text that modifies the first artist's name. | attribué à |  |  |
|  attribution_auth_mod1 | alphabetic | blank | Authority text of modifier used for Linked Open Data model. | attribué à |  |  |
|  artist_ulan_id_1 | numeric | blank | ULAN ID for first artist authority | 500014268 |  |  |
|  title | alphabetic | blank | Titles are transcribed exactly as they appear in the stock books, including the spelling and punctuation. | Paysage avec moutons |  | Where possible, abbreviations are spelled out and shortcuts such as "do" and "idem" are replaced by the actual title or term referenced. The title "`[sans titre]`" is added when a title could not be found.  |
|  description | alphabetic | blank | Verbatim notes about provenance or purchase. | Ancien no 2104 |  |  |
|  subject | alphabetic | blank | One or more terms from a small controlled vocabularly developed by PSCP to describe the subject of an object. | Architecture, Batailles, Intérieurs, Marines, Militaire, Mythologie (figures), Mythologie (narratif), Paysage avec figures, Religieux (figures), Religieux (narratif), Ruines, Sporting, Vues topographiques |  | Terms are more granular than genre terms (see below). For example, an object titled "La Vierge à l'Enfant" would be assigned the genre term "Histoire" and the subject term "Religieux (figures)". Multiple values are concatenated with semi-colons. |
|  genre | alphabetic | [not identified] | One term or more terms from a small controlled vocabulary developed by PSCP to describe the category of composition of the object. | Animaux; Genre; Historie, Nature Morte, Paysage, Portrait |  | Categories are based on the hierarchy of genres established by the French Academy in the 17th century (see Examples). Multiple values are concatenated with semi-colons. |
|  object_type | alphabetic | blank | One term or more terms describing the kind of object. | Aquarelle; Dessin; Peinture; Sculpture; Tapisserie |  |  |
|  materials | alphabetic | blank | Text describing the materials of object. | Argent; Esquisse au crayon; Gouache; Mine de plomb; Papier; Porcelain |  |  |
|  dimensions | alphanumeric | blank | Text describing the dimensions of the object. | 101 1/2 x 68 1/2 |  | Dimensions for rectangular objects are given in this order: height, width, length. Other units may be used as appropriate for the object. |
|  entry_date_year | numeric | blank | Year in which object entered the dealer's stock. For completeness, the year of the entry has been added in brackets when it does not appear in the stock book. | 1875 |  | If the same work was inventoried later, the entry year remains the same. |
|  entry_date_month | numeric |  | Month of the year in which object entered the dealer's stock. | 5 |  | If the same work was inventoried later, the entry month remains the same. |
|  entry_date_day | numeric |  | Day of the month in which object entered the dealer's stock. | 15 |  | If the same work was inventoried later, the entry day remains the same. |
|  sale_date_year | numeric | blank | If sold, year in which transaction took place. | 1882 |  |  |
|  sale_date_month | numeric |  | If sold, month in which transaction took place. | 6 |  |  |
|  sale_date_day | numeric |  | If sold, day on which transaction took place. | 26 |  |  |
|  purch_amount | numeric | blank | Total amount paid by the dealer for the object. | 7500 |  | Occasionally, a code like those used in cost_translation (see below) is used, in which case this field contains the translated code. |
|  purch_code |  |  | Code for amount dealer paid for the object. | TANN |  |  |
|  purch_currency | alphabetic | blank | Currency with which the dealer paid for the object. | francs |  |  |
|  purch_frame | alphanumeric | blank | Price paid or other information about the frame | cadre 50 francs<br/>cadre compris |  |  |
|  purch_note | alphabetic | blank | Additional information about the dealer's purchase of the object. | pour 106a & 106b<br/> |  | If the price was paid for multiple objects, such information will appear here. |
|  purch_ques | alphabetic | blank | If there is uncertainty about the purchase price, this field contains a "?" in brackets. | ? |  |  |
|  purch_loc | alphabetic | blank | Location at which purchase was made | Arthur, Tooth & Sons, 155, New Bond Street, Londres |  | Purchase locations, often mentioned in the "Stock Book Notes" column in the Goupil stock books, are formatted as place, city, and country. Locations most often cited are branches of Goupil & Cie. |
|  purch_loc_note | alphabetic | blank | Additional information about the purchase location. | Chevallier, commissaire priseur |  |  |
|  cost_code | alphabetic | blank | Code for dealer's cost of preparing the object for sale. | NUO |  | Dealer cost codes are more commonly referred to as production costs in galleries today. |
|  cost_translation | alphabetic | blank | Translation of code for dealer's cost preparing the object for sale. | 483 |  | The cost codes have been translated according to the following schemes, which were handwritten by Dieterle on the title page of almost all of the stock books:<br/>for stock books 1-7: A=1; M=2; O=3; N=4; S=5; I=6; E=7; U=8; R=9; X=0; Z=0 ("a monsieur")<br/>for stock books 8-15: P=1; R=2; E=3; C=4; A=5; U=6; T=7; I=8; O=9; N=0; X=0; Z=0 Y=0 ("precaution") |
|  cost_currency | alphabetic | blank | Currency with which the dealer's cost was paid. | francs |  |  |
|  cost_frame | alphanumeric | blank | Amount (with currency) dealer spent on frame. | cadre 40 francs |  |  |
|  cost_description | alphabetic | blank | Additional information about the dealer's cost | Pour les nos 1015[a] & 1015[b] |  | If the price was paid for multiple objects, such information will appear here. |
|  cost_number | numeric | blank | Number that appears in stock book next to dealer's cost. | 700 |  | The meaning of this number is not currently known. |
|  **Multiple groups of price fields, numbered sequentially from _1 to _2, may occur.** |  |  |  |  |  |  |
|  price_amount_1 | numeric |  | Amount paid by the buyer to the dealer. | 6700 |  |  |
|  price_code_1 | alphabetic |  | Code for amount paid by the buyer to the dealer. |  |  | See cost_translation (above) for schemes used to translate codes for numeric price_amount. |
|  price_currency_1 | alphabetic |  | Currency in which the buyer paid the dealer. | francs |  |  |
|  price_note_1 |  |  | Additional information about the sale price. | les no 669 & 670 pris en échange du no 600 |  |  |
|  **Multiple groups of seller name fields, numbered sequentially from _1 to _2, may occur.** |  |  |  |  |  |  |
|  seller_name_1 | alphabetic | blank | Verbatim name of the first seller. | Boussod Valadon & Co |  |  |
|  seller_loc_1 | alphabetic | blank | Verbatim location of the first seller. | Paris |  |  |
|  sell_auth_name_1 | alphabetic | blank | Authority name for first seller, established by PSCP. | Boussod, Valadon et Cie. |  |  |
|  sell_auth_loc_1 | alphabetic | blank | Authority location for first seller, established by PSCP. | Paris, France |  |  |
|  sell_auth_mod_1 | alphabetic | blank | Authority text that supplies additional information about the first seller, in relation to the second seller. | for |  | If there was an agent relationship between the primary seller and an intermediary such information will appear here. |
|  seller_ulan_id_1 | numeric |  | ULAN ID for first seller authority | 500447965 |  |  |
|  **Multiple groups of joint owner name fields, numbered sequentially from _1 to _3, may occur.** |  |  |  |  |  |  |
|  joint_own_1 | alphabetic | blank | Name of first joint owner. | Wallis |  |  |
|  joint_own_sh_1 | alphanumeric | blank | Fractional share owned by first joint owner | 1/2 |  |  |
|  joint_ulan_id_1 | alphanumeric | blank | ULAN ID for first joint owner | 500435647 |  |  |
|  transaction | alphabetic | blank | Indicates sale status of the object.  | Vendu |  |  |
|  **Multiple groups of buyer name fields, numbered sequentially from _1 to _2 may occur.** |  |  |  |  |  |  |
|  buyer_name_1 | alphabetic | blank | Verbatim name of first buyer. | Chaine & Simonson |  |  |
|  buyer_loc_1 | alphabetic | blank | Verbatim location of first buyer. | Paris |  |  |
|  buyer_mod_1 | alphabetic | blank | Text that supplies additional information about the primary buyer. | [par] La Haye |  |  |
|  buy_auth_name_1 | alphabetic | blank | Authority name for first buyer, established by PSCP. | Chaine & Simonson, J. |  |  |
|  buy_auth_addr_1 | alphabetic | blank | Authority location for first buyer, established by PSCP. | Paris, France |  |  |
|  buy_auth_mod_1 | alphabetic | blank | Text that supplies additional information about the primary buyer. | par Succursale de La Haye, Pays-Bas. |  | If there was an agent relationship between the primary buyer and an intermediary such information will appear here. |
|  buyer_ULAN_ID_1 | numeric |  | ULAN ID for first buyer. | 500443250 |  |  |
|  previous_owner | alphabetic | blank | Notes about owner(s) of object prior to current transaction described | Georges Petit |  | Multiple values are concatenated with semi-colons. |
|  previous_sales | alphabetic | blank | Notes about sales that included the object before the current transaction. | Vente Troyon |  |  |
|  post_sales | alphabetic | blank | Notes about sales that included the object after the current transaction. | Galerie d'un amateur de Vienne, Vente les vendredi 27 et samedi |  |  |
|  post_owner | alphabetic | blank | Notes about the owners of the object following the current sale. | 1898 achete par W.R. Hearst chez Knoedler |  | Multiple values are concatenated with semi-colons. |
|  sale_location | alphabetic | blank | Location at which sale was made. | Le Haye<br/>Exposition de Rotterdam<br/>Hôtel des ventes, Paris, France. |  |  |
|  present_loc_geog | alphabetic | blank | Present location, if known, including city, state, country, of the owning institution. | Nantes, France |  |  |
|  present_loc_inst | alphabetic | blank | Name of present owning institution, if known. | Musée des Beaux-Arts |  |  |
|  present_loc_acc | alphanumeric | blank | Accession number in collection of present owning institution, if known. | 87.15.130 |  |  |
|  present_loc_note | alphabetic | blank | Text that supplies additional information about the owning institution. | as "Ovide among the Scythians" |  |  |
|  present_loc_ulan_id | numeric |  | ULAN ID for present owning institution. | 500303422 |  |  |
|  working_note | alphabetic | blank |  | Colonnes n., sujet, genre, artiste, date entree, prix de revien | See verbatim_notes |  |
|  verbatim_notes | alphabetic | blank | All notes and miscellaneous information from the stock book entry are combined into this field. May contain editorial notes added for clarification. | suprimé, vendu par Mr Uls |  | All notes and miscellaneous information from the stock book entry are combined into this field. May contain editorial notes added for clarification. |
|  editor_notes | alphabetic | blank | All research notes and remarks from the PSCP editors. | Il n'est pas certain que le nom de l;acheteur soit "La Haye" | See verbatim_notes |  |
|  no_name_notes | alphabetic | blank | Information from a column in the stock books that was untitled. | NY P55 |  |  |
|  rosetta_handle | alphanumeric | blank | URL for an image of the stock book page on which the record appears | http://hdl.handle.net/10020/900239_FL1647151 |  |  |



