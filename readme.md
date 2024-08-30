# Moeilijke woorden lijst voor Textlint

Lijst met moeilijke woorden van [Onze Taal](https://onzetaal.nl/taalloket/modern-taalgebruik) die gebruikt kan worden met [textlint](https://github.com/textlint/textlint) en [textlint-rule-terminology](https://github.com/sapegin/textlint-rule-terminology). Door teksten te linten, kunnen moeilijke woorden in teksten geworden gevonden.

Moeilijke woorden zijn slecht voor de toegankelijkheid van een site. In [WCAG richtlijn 3.1.3](https://digitaaltoegankelijk.nl/wcag-uitgelegd/3-1-3-ongebruikelijke-woorden-wcag-niveau-aaa/) wordt aangeraden om moeilijke woorden te vermijden of uit te leggen.

## Let op

[textlint-rule-terminology](https://github.com/sapegin/textlint-rule-terminology) kan woorden automatisch vervangen door betere alternatieven. Dit is niet aan te raden omdat een andere woordkeuze vaak ook betekent dat een zin anders geformuleerd moet worden. Gebruik dus geen "--fix".

## Installatie

Installeer eerst [textlint](https://github.com/textlint/textlint) en [textlint-rule-terminology](https://github.com/sapegin/textlint-rule-terminology). Daarna:

```bash
npm i moeilijke-woorden
```

Voeg de lijst toe aan het configuratiebestand van textlint.

>.textlintrc.json

```json
{
  "plugins": {},
  "filters": {},
  "rules": {
    "stop-words": true,
    "terminology": {
      "terms": "../../moeilijke-woorden/moeilijke-woorden.json"
    }
  }
}
```

## Gebruik

Zoals textlint

```bash
npx textlint [file]
```
