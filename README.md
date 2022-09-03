# Scrape-IPA-wordlists-from-Wiktionary

This code scrapes Wiktionary (https://en.wiktionary.org/w/index.php?title=Category:Terms_with_IPA_pronunciation_by_language&from=F) to produce IPA wordlists composed all the words of a given language for which an IPA transcription is provided in Wiktionary. The output is a csv file containing the IPA transcription and dialect tag (if specified by Wiktionary) of each word, but no translation. An example of output file is provided in this repository.

The output is produced by executing one function: scrapeFromWiktionaryIPAwords(language), which takes the language of interest as its unique argument.

Executing this function requires:
- to install Selenium and a driver to interface with the chosen browser (instructions here: https://selenium-python.readthedocs.io/installation.html)
- To replace "" in the code by the path to the place you chose for the driver on your computer
- an Internet connection
- to use the same language name as Wiktionary (e.g. "Occitan", "Haitian Creole")

The execution of the script takes approximately 01:05 minute per 200 entries (=1 Wiktionary page) on my laptop. For scraping the French IPA wiktionary (79825 entries), it would hence take approximately 07:15 hours to run.

DISCLAIMER: The HTML structure of Wiktionary varies slitghtly from language to language. This script is intended to be quite robust, but I cannot guarantee that it works perfectly for all languages of Wiktionary.


