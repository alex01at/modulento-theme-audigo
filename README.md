# Audigo

A site theme for [Modulento](https://github.com/alex01at/modulento) for an
auction house: a dark hero with a live sign, lot cards that show the current
price, and a home page that is made of blocks an administrator can change.

It brings a layout, a home page (hero with search, category tiles, the running
auctions, three steps, the auction houses and a call to become a seller), card
partials for lots and providers, a stylesheet and its font. Every other page
comes from Modulento's `default` theme and only looks different.

The lots are offers of the type `auction.lot` of the **Auctions** extension
(`alex01at/modulento-ext-auction`). The theme does not bring bidding itself: the
bid form, the countdown and the bid history are the extension's, on the lot's
page. Install the extension for auctions to take place at all.

## Editing in place

From the first start, the home page is editable with **Administration** rights:
open the home page with `?edit=1` (the pencil in the header). A click on a text
edits it on the spot, a "+" between the blocks adds one, and each block can be
duplicated, hidden, saved as a widget or dragged to another place. The lot page
has the same tools for its own texts.

The start page is in `home-layout.json`; once an administrator saves the page,
the stored one applies.

## Installing

In Modulento, open **Administration → Packages**, enter
`alex01at/modulento-theme-audigo` and install. Then choose "Audigo" under
**Administration → Themes**. New versions appear on the Packages page.

By hand: unpack a release into `themes/audigo/` of the installation.

## Changing the wording

The texts of the theme are in `lang/de.php` and `lang/en.php`, with keys
starting `theme.`. Do not edit them here - an update would replace the file.
Put your own wording into `lang/<language>.php` of the installation.

## Colours

Every colour in `assets/theme.css` is a variable on `:root`. The dark scheme
follows the device, unless an account has chosen "light" or "dark"; both dark
blocks below `:root` carry the same values.

## Development

No build step. The package is the repository without the files listed in
`.gitattributes`; a tag `vX.Y.Z` that matches `version` in `theme.json` makes
the release, which carries the package and its checksum.
