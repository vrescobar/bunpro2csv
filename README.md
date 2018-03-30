# bunpro2csv

tampermonkey script to export/backup a bunpro grammar point to csv (and then import to Anki if that is your wish).

Note: because of technical reasons the CSV separator character is a vertical slash: ```|```.

# Motivation

I believe not every webpage should have their own integrated SRS mechanism, there are other SRS systems far more superior such as anki or supermemo.

Having to use SRS services in 4 or 5 different webpages is unsupportable for anyone and with this system bunpro users get the missing feature: use your own SRS system.

Taking notes in your classes is a complete legal practice; also to share it with your acquitances and colleagues as long as it is a private activity without lucrative goals. This is the main aim of this script: the private usage of the information you are learning and a shortcut from the studied materials to your favourite SRS program.

Please do not reupload somewhere either public distribute the backed-up contents from your account (notice that no batch download has been implemented, only one grammar point and a time).

# install into tampermoneky/greasemonkey

Make sure you installed the extension "tampermonkey" in your browser. Then Add the ```bunpro2cvs.js``` script to it (click add new script and then copy paste its contents).


# usage with a UI button

Install the script in your tampermonkey browser plugin and you will automagically see the download button in any grammar point.

After you refresh your bunpro page you will see something like that.

![import dialogue](img/スクリーンショット01.jpg?raw=true)


# usage from the developer tools

Tested only on google chrome and safari.

1.- Browse to the grammar point you want to backup.
2.- Open the developer tools panel (usually contol + J) and find the javascript console
3.- copy and paste the function ```download_grammar_point``` from the ```bunpro2cvs.js``` file.
4.- type in the javascript console ```download_grammar_point()```
5.- Your download should have started automatically.


# How to import to Anki

Anki users probably already invested a bit of money to get cloud sync and native apps for their desktops and mobiles so they might be the ones

1. Open Anki
2. Create a deck called _my bunpro studied grammar_ or whatever you find convenient.
3. Create a new card type with 7 fields as you can see in the screenshor bellow.
4. Click on _File_ -> _Import..._ and in the dialogue select your new card type for this action. 
5. It is very important that you mark that the fields are separated by the character ```|``` instead of the usual colon character.
6. Allow HTML, ignore duplicates... and click on import.
7. Create a beautiful template for your cards. I provide my simple ones in the ```anki_template``` [subfolder](anki_template/). However, do not waste your time with inputting the text in anki... better write them on paper or use the actual bunpro page if that is a major concern for you.
8. Make sure you sort your cards by the index field, you might want to use anki plugins for that (however if you already studied the grammar that should not be a major issue either).

![A new card with the next fields](https://github.com/vrescobar/bunpro2csv/blob/master/img/スクリーンショット00.jpg)
![import dialogue](https://github.com/vrescobar/bunpro2csv/blob/master/img/スクリーンショット02.jpg)
![the | separator for the CSV](https://github.com/vrescobar/bunpro2csv/blob/master/img/スクリーンショット03.jpg)



# Legal concerns

Mass distribution of partly or completely ripped contents might be illegal in your country and definetly a punished commercial practice in Europe. *Please do not reupload, share or resell any of the downloaded contents.*


# Contributions, usage and license

I created this script to my own personal use because that was the fastest way for me to get this feautre. now I want to give back to the community which has contributed largely and without interest to many learning resources.

I won't update or improve the script after PRs, if you want this feature so bad please consider asking the bunpro administrators for it.

The script is licensed as MIT (aka you can do whatever you want with it).
