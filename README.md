# HupiCast

**HupiCast** on Android-sovellus, jonka tarkoituksena on peilata puhelimen näyttö yhteensopivaan HupiCastTV-sovellukseen lähiverkon kautta.

## Ominaisuudet

- 📱 Puhelimen näytön peilaus televisioon.
- 📺 Yhteys HupiCastTV-sovellukseen saman Wi-Fi-verkon kautta.
- 🔍 Television automaattinen etsiminen lähiverkosta.
- 🔢 Kuusinumeroinen parituskoodi.
- 🖼️ Näytön kuvien lähettäminen televisioon JPEG-muodossa.
- ⏹️ Peilauksen pysäyttäminen ja yhteyden katkaiseminen.
- 🌐 Tiedonsiirto paikallisverkon TCP-yhteydellä.

## Sovellukset

HupiCast koostuu kahdesta sovelluksesta:

| Sovellus | Tarkoitus |
|---|---|
| **HupiCast** | Puhelimen näytön lähettäminen |
| **HupiCastTV** | Näytön vastaanottaminen ja näyttäminen televisiossa |

## Käyttöönotto

1. Asenna HupiCast-puhelinsovellus Android-puhelimeen.
2. Asenna HupiCastTV-sovellus yhteensopivaan Android TV -laitteeseen.
3. Yhdistä molemmat laitteet samaan Wi-Fi-verkkoon.
4. Käynnistä HupiCastTV ja odota, että sovellus käynnistyy.
5. Avaa HupiCast puhelimessa ja etsi televisio.
6. Hyväksy Androidin näytönkaappauslupapyyntö.
7. Aloita peilaus ja varmista, että kuva näkyy televisiossa.

## Tekniikka

- **Alusta:** Android
- **Ohjelmointikieli:** Kotlin
- **Näytönkaappaus:** Android MediaProjection API
- **Laitteiden löytäminen:** Android Network Service Discovery (NSD)
- **Verkkoyhteys:** TCP
- **Portti:** `8765`
- **Kuvamuoto:** JPEG

### Tiedonsiirto

1. Puhelin löytää HupiCastTV-palvelun lähiverkosta.
2. Puhelin lähettää kuusinumeroisen parituskoodin.
3. Televisio hyväksyy yhteyden, jos koodi täsmää.
4. Puhelin kaappaa näytön kuvia ja lähettää ne TCP-yhteydellä.
5. HupiCastTV vastaanottaa kuvat ja näyttää ne näytöllä.

## Tietosuoja

HupiCast on suunniteltu siirtämään peilattava näyttökuva paikallisverkon kautta. Näytön sisältö voi sisältää henkilökohtaisia tietoja, joten peilausta kannattaa käyttää vain luotettavassa verkossa ja omien laitteiden kanssa.

Android pyytää käyttäjältä luvan näytön kaappaamiseen. Sovelluksen todellinen tietojen käsittely riippuu käytössä olevasta versiosta ja toteutuksesta.

## Vaatimukset

- Android-puhelin, joka tukee tarvittavia MediaProjection-ominaisuuksia.
- Yhteensopiva Android TV -laite tai muu Android-laite, jossa HupiCastTV toimii.
- Molemmille laitteille yhteinen lähiverkko.
- Verkon palomuurin tulee sallia TCP-yhteys porttiin `8765`.

## Vianmääritys

**Televisio ei löydy**
- Varmista, että laitteet ovat samassa Wi-Fi-verkossa.
- Tarkista, ettei reitittimen asiakaseristys estä laitteiden välistä yhteyttä.
- Käynnistä HupiCastTV uudelleen ja yritä etsiä televisio uudelleen.

**Kuva ei näy**
- Tarkista näytönkaappauslupa.
- Varmista, että yhteys muodostuu porttiin `8765`.
- Tarkista, että HupiCastTV on käynnissä.

**Yhteys katkeaa**
- Tarkista Wi-Fi-yhteys ja verkon palomuuriasetukset.
- Varmista, ettei toinen sovellus tai palvelu käytä samaa porttia.

## Projektin tila

HupiCastin ominaisuudet ja yhteensopivuus riippuvat käytössä olevasta sovellusversiosta. Kaikkia laitteita ja Android-versioita ei ole välttämättä testattu.

## Lisenssi

Lisenssiä ei ole määritelty tässä README-tiedostossa. Lisää projektin oma lisenssi, jos julkaiset lähdekoodin muiden käytettäväksi.
