# cryptoBRO

**Din personlige kryptoassistent.** Et dashbord for kryptomarkedet med live priser, grafer, nyhetsanalyse, trading-verktøy, en lærende øve-agent og et komplett kurs i krypto og trading. Alt ligger i én fil og kjører rett i nettleseren.

**Åpne appen:** https://andha123.github.io/crypto-bro/

Appen er laget for mobil (iPhone og Android) og fungerer også på PC. Den finnes på norsk og engelsk.

---

## Hva appen gjør

- Viser **live priser** for kryptovalutaer, med endring siste time, døgn og uke.
- Gir en **daglig oversikt** over markedet: stemning, viktige hendelser og nyheter.
- Har **ryddige grafer** der du selv velger mellom linje og candlesticks.
- Lar deg **analysere og planlegge trades** med støtte, motstand, signaler, stop loss, target og risk/reward.
- Har en **trading-agent** som handler med 1000 falske dollar og lærer av sine egne feil.
- Har et **kurs med eksamen**: 7 moduler, 75 temaer og 300 oppgaver.
- Sender **varsler** som små bokser i hjørnet. De samles under bjella øverst til høyre.

## Sidene i appen

| Side | Hva du finner der |
|---|---|
| **Hjem** | Personlig hilsen som endrer seg etter tid og marked, nøkkeltall, «Dagens hendelser» og AI-oppsummering av dagen |
| **Marked** | Oversikt, alle mynter, sektorer og prisgraf (linje eller candles) |
| **Trading** | Live analyse av grafen, «Plan og risiko» og demotrading. Velg mellom graf, analyse eller begge |
| **Agent** | Øve-agenten: verdi over tid, åpne posisjoner, alle handler og hva den har lært |
| **Toppliste** | Myntene som har steget og falt mest |
| **Nyheter** | Bare relevante nyheter, sortert nyest først, med oppsummering og mulig betydning for markedet |
| **Kalender** | Kalender i Apple-stil (dag, uke, måned, år) med rentemøter, inflasjonstall og andre hendelser |
| **Fear & Greed** | Markedsstemningen fra 0 til 100, med historikk |
| **Mine mynter** | Dine egne mynter og favoritter |
| **Varsler** | Prisvarsler |
| **Lær** | Kurset, ordliste og verktøy |
| **Mynt-sider** | Trykk på en mynt for å se hva den er, fordeler, ulemper, risiko, graf og nyheter. Spørsmålstegnet «?» gir en rask forklaring |

De tre knappene i midten av menyen nederst kan du velge selv under **Innstillinger**. Der kan du også bytte tema, farge og språk, og eksportere eller importere dataene dine.

## Kurset

Kurset ligger under **Lær → Kurs** og bygger på trading-dokumentet appen er laget rundt.

1. Grunnleggende kryptokunnskap (10 temaer)
2. Tradingbegreper (10)
3. Candlesticks og teknisk analyse (14)
4. Entries og tradeplanlegging (11)
5. Risk management (10)
6. Markedsanalyse (10)
7. Tradingpsykologi og disiplin (10)

**Slik fungerer det:**

- Du leser leksjonen først. Den har forklaringer, figurer, begreper, et eksempel fra kryptomarkedet og en oppsummering.
- Oppgavene starter når du trykker **«Gå videre til oppgaver»**. Du får én oppgave om gangen, og mange av dem bruker candlestick-grafer.
- Etter **«Bekreft svar»** ser du med en gang om svaret var riktig, med forklaring. Svaret kan ikke endres etterpå.
- Et tema er **bare bestått når alle svarene er riktige**. 3 av 4 riktige gir ikke delpoeng.
- **Kursprosent = beståtte temaer ÷ 75 × 100.** Et bestått tema forblir bestått selv om du øver på det igjen.

## Trading-agenten

Agenten handler helt på egen hånd med **1000 falske dollar**. Den bruker ekte priser, men ikke ekte penger. Du kan bare følge med.

- Den følger reglene i trading-dokumentet: støtte og motstand, candle-signaler, trend, R:R på minst 1,5 og fast risiko per trade.
- Den bruker giring fra 1x til 100x, og sammenligner seg med å kjøpe og holde bitcoin eller en kurv med de 10 største myntene.
- Den **lærer av hver avsluttede trade**. Den dropper oppsett som har tapt penger, senker giringen etter likvideringer, krever høyere R:R hvis lave R:R taper, gir stop loss mer rom ved mye støy og halverer risikoen etter tapsrekker.
- Alt den lærer, vises i boksen **«Hva agenten har lært»** og i en læringslogg.

Agenten har ingen egen server. Den jobber mens appen er åpen, og spiller av timene den gikk glipp av når du åpner appen igjen.

## AI-funksjoner

Noen knapper bruker Claude fra Anthropic: dagens oppsummering, grundig nyhetssøk, forklaring av mynter og nyhetssaker. Til dette trenger du en egen **API-nøkkel** fra [console.anthropic.com](https://console.anthropic.com).

- API-bruk betales per bruk og er ikke inkludert i et Claude Pro-abonnement.
- Resten av appen er gratis og trenger ingen nøkkel.

## Data og kilder

| Data | Kilde |
|---|---|
| Priser og markedsdata | CoinGecko (reserve: Coinpaprika) |
| Live priser | Binance |
| Candlesticks | Bybit (reserve: OKX og Coinbase) |
| Fear & Greed | alternative.me |
| Nyheter | RSS-feeder fra blant annet CoinDesk, Cointelegraph, Decrypt, CryptoSlate, Blockworks og Google News |
| AI | Anthropic Claude (valgfritt, med egen nøkkel) |

## Personvern og lagring

- Appen har **ingen innlogging og ingen egen server**.
- Innstillinger, kursfremgang, agentens historikk og API-nøkkelen lagres **bare i nettleseren på enheten din** (localStorage). Ingenting synkroniseres mellom enheter.
- API-nøkkelen sendes bare til Anthropic (`api.anthropic.com`) når du bruker en AI-knapp.
- Under **Innstillinger** kan du eksportere dataene til en fil og importere dem på en annen enhet.

## Slik oppdaterer du appen

Hele appen er filen `index.html`.

1. Gå til **Add file → Upload files** i dette repoet.
2. Last opp den nye `index.html`. Filen må hete nøyaktig `index.html`.
3. Trykk **Commit changes**.
4. Vent 1–2 minutter. Last siden på nytt hvis du fortsatt ser den gamle versjonen.

## Viktig

cryptoBRO er laget for **læring og oversikt**. Ingenting i appen er investeringsråd. Analyser, signaler og agentens handler er regelbaserte og kan ta feil. Trading med giring kan gi tap av hele innsatsen på kort tid. Øv med demotrading før du bruker ekte penger, og bruk bare penger du har råd til å tape.
