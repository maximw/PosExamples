# PieceofScript examples

Example scenarios for <a href="https://github.com/maximw/PieceofScript">PieceofScript</a>. 

### Installation
You need have installed PHP 7.2 or higer.

Clone repository

```
git clone https://github.com/maximw/PosExamples.git
cd ./PosExamples
```

Download PieceofScript phar

```
wget https://github.com/maximw/PieceofScript/raw/master/bin/pos.phar
```

or you can <a href="https://github.com/maximw/PieceofScript/blob/master/docs/usage.md#usage">compile pos.phar</a> by yourself.

Now you are prepared to start testing.

### Pastery

<a href="https://www.pastery.net/">Pastery</a> is similar to Pastebin.com. <a href="https://www.pastery.net/api/">API documentation</a>.

You need to <a href="https://www.pastery.net/login/">get key</a> before use Pastery API and put it to ./Pastery/globals.pos file.

```
php pos.phar run ./Pastery/start.pos -r pastery_report.html -vvv
```

### Rick and Morty

The Rick and Morty API is based on the television show Rick and Morty. It provides information about hundreds of characters, images, locations and episodes. 
<a href="https://rickandmortyapi.com/documentation/#rest">API documentation</a>.

```
php pos.phar run ./RickAndMorty/20MinutesTest.pos -r shlapi_report.html -vvv
```

### Virustotal

<a href="https://www.virustotal.com/">Virustotal</a> analyzes suspicious files and URLs to detect types of malware. <a href="https://developers.virustotal.com/reference">API documentation</a>.

I wrote tests only for public part of API, except Comments endpoints.

File ./Virustotal/files/hiddeninput.exe is from Symfony Console component. You can delete it and analyze any other file up to 32 Mb (API limitation).

You need to <a href="https://www.virustotal.com/gui/join-us">get key</a> before use Virustotal API and put it to ./Virustotal/globals.pos file.

```
php pos.phar run ./Virustotal/start.pos -r virustotal_report.html -vvv
```