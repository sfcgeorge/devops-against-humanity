# Devops Against Humanity

DevOps Against Humanity (an expansion for [Cards Against Humanity](http://www.cardsagainsthumanity.com))

Because people on twitter are hilarious.

This repo is a fork, with the goals of modifying this expansion to:

* Use a format suitable for use in the bbcards generator.
* Have a number of cards that [this print company](http://www.printerstudio.com/personalized/custom-playing-cards-gifts.html) can print.
* A better icon(s) that work on black and white cards.
* Cards that I think even non devopsy people can somewhat understand, hopefully.

### Card Ideas

There's a Google doc here:

[Shared Google Doc](https://docs.google.com/spreadsheets/d/1OKgmjNz8l7skYfrbrOtYT6QmSf_y-BzZOWJWZC3tbUQ/edit#gid=0)

Add your awesome ideas to the shared doc. Then copy it, edit it to your liking, sorting and removing anything you don't like. Suggested going with a standard of five underscores for each blank, since otherwise they can take up too much room on the cards.

This is a doc that the original repo owner used for generating their cards:

[Doc used for first printing](https://docs.google.com/spreadsheets/d/1LEf6qE3FMKRvSWRrKb3m5gcVHmw7aQctbegrWbxEsfA/edit?usp=sharing)

I'm basing my modification of the original creator's expansion on these docs, but formatted for use in bbcards generator and cards selected to be hopefully vaguely understood by even non devopsy people.


### Format for PDF Generation

I'm using my [fork of bbcards](https://github.com/sfcgeorge/bbcards) for PDF generation. This means there is one plain text file for black cards, and one for white cards. Each card is separated by a blank line. Blanks are represented by 5 underscores, by convention. Inline HTML can be included to add basic formatting to the cards, but it is recommended to not overuse this.


### Generating the PDFs

I [forked bbcards generator](https://github.com/sfcgeorge/bbcards) to add a bleed area as required by this printing company. So, with that fork and this repo of card files what you have to do to generate a PDF of the cards is:

1. Install Ruby, tested on 2.1 but 1.9.X should work fine too. The script uses Helvetica font, which is included on Macs but I'm not sure what happens on Windows or Linux, perhaps a compatible Helvetica derivative is bundled somewhere.
2. CD into this repo's directory, so the bbcards generator can pick up the icon files.
3. `ruby /path/to/your/clone/of/bbcards/bbcards.rb -l -p -n "Devops Against Humanity" -d .`
4. You will then need to convert the PDF into PNG images to send to the printer, use a high DPI for sharp text. The print company recommends at least 300 DPI which is alright, but go for 1200 DPI.


### Printing

I chose [this printing company](http://www.printerstudio.com/personalized/custom-playing-cards-gifts.htmlruby /Users/sfcgeorge/Documents/Projects/Design/bbcards/bbcards.rb -l -p -d .) because they will print a lot of cards (234) for very cheap ($21.54). They offer 310gsm cardstock with linnen texture very similar to the official cards, and in the same poker size with rounded corners. So if you print this expansion with them it should match the official cards fairly closely. My [fork of bbcards](https://github.com/sfcgeorge/bbcards) generates the correct bleed area for this printer.


### Licence

From the CAH website: "Cards Against Humanity is available under a Creative Commons BY-NC-SA 2.0 license. That means you can use and remix the game for free, but you can’t sell it. Please do not steal our name or we will smash you." This version is called Devops Against Humanity and isn't being sold. It is intended that you buy the original game from the source, then make this expansion to add.
