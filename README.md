# Vabanenud õppekohad Tartu Ülikoolis - uus kujundus

## Andmete muutmise kuupäev

Andmete muutmise kuupäeva kuvamiseks on funktsioon. 
Andmete muutmise kuupäev ja kellaaeg tuleb sisestada index.html faili reale 144.

## Andmed tabelisse
Tabelisse loetakse andmed .json vormingus failist, mis asub serveris samas kaustas muude failidega. 
Fail nimetus peab olema andmed.json
.xlsx failist .json faili tekitamiseks on mitmeid konvertereid, nt 
[SEDA](https://www.cloudmersive.com/convert-xlsx-to-json-tool) - ei tee fail, teeb järjendi, mis tuleb kopeerida ja faili sisusse kleepida, aga muidu neist konverteritest, mis ma leidnud olen, kõige parem, st saab täpitähtedega hakkama, ei kaota ridu.
Tabelis kuvatakse andmed samas järjestuses, nagu need on failis.
Failis peavad andmed olema sellisel kujul:

```
[
    {
        "Valdkond":"HV",
        "Tase":"511",
        "Kood":"2435",
        "Õppekava":"Ajalugu",
        "1. aasta PÕ":"3",
        "1. aasta SÕ":"",
        "2. aasta PÕ":"4",
        "2. aasta SÕ":"",
        "3. aasta PÕ":"10",
        "3. aasta SÕ":"",
        "4. aasta PÕ":"",
        "4. aasta SÕ":"",
        "5. aasta PÕ":"",
        "5. aasta SÕ":"",
        "6. aasta PÕ":"",
        "6. aasta SÕ":""
        },
    {
        "Valdkond":"HV",
        "Tase":"511",
        "Kood":"2429",
        "Õppekava":"Antiikkeeled ja -kultuurid", 
        "1. aasta PÕ":"1",
        "1. aasta SÕ":"",
        "2. aasta PÕ":"4",
        "2. aasta SÕ":"",
        "3. aasta PÕ":"6",
        "3. aasta SÕ":"",
        "4. aasta PÕ":"",
        "4. aasta SÕ":"",
        "5. aasta PÕ":"",
        "5. aasta SÕ":"",
        "6. aasta PÕ":"",
        "6. aasta SÕ":"",
    }
]
```

## Otsing
Otsinguga otsitakse otsisõna väärtust tabeli veergudest “Valdkond”, “Tase”, “Kood” ja “Õppekava”. Peidetakse tabeli read, kus otsitavat ei leidu.

## Pildid
Favicon, Tartu Ülikooli logo ja päise foto asuvad kataloogis img.
Vaba koha foto autor on Mairi Saar.

## Üldine
Leht on seadme laiusega kohanduv. Kitsamal ekraanil (nt mobiil) kuvatakse tabeli teistsugust vaadet.
Iga tabeli rida kuvatakse eraldi plokina. 
Peidetakse need veerud, kus andmeid ei ole (nt kui mingi õppekava 2. aasta SÕ vabu kohti ei ole, siis seda veergu (reana) ei kuvata.
