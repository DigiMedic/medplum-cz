# [Medplum](https://www.medplum.com) &middot; [![GitHub licence](https://img.shields.io/badge/license-Apache-blue.svg)](https://github.com/medplum/medplum/blob/main/LICENSE.txt) [![npm verze](https://img.shields.io/npm/v/@medplum/core.svg?color=blue)](https://www.npmjs.com/package/@medplum/core) [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=medplum_medplum&metric=alert_status&token=207c95a43e7519809d6d336d8cc7837d3e057acf)](https://sonarcloud.io/dashboard?id=medplum_medplum) [![Coverage Status](https://coveralls.io/repos/github/medplum/medplum/badge.svg?branch=main)](https://coveralls.io/github/medplum/medplum?branch=main)

![Medplum](packages/docs/static/img/cover.webp)

Medplum je vývojářská platforma, která umožňuje flexibilní a rychlý vývoj zdravotnických aplikací.

- **Medplum Auth** - End-to-end řešení identity pro snadné ověřování uživatelů, přihlašování a oprávnění pomocí OAuth, OpenID a SMART-on-FHIR.
- **Medplum Clinical Data Repository (CDR)** - Backendový server, který hostí vaše zdravotnická data v bezpečném, kompatibilním a na standardech založeném úložišti.
- **Medplum API** - Rozhraní API založené na FHIR pro odesílání, příjem a manipulaci s daty.
- **Medplum SDK** - Klientské knihovny, které zjednodušují proces interakce s rozhraním **Medplum API**.
- Aplikace **Medplum** - webová aplikace, ve které si můžete prohlížet data a provádět základní editační úlohy. Aplikaci Medplum App můžete také použít ke správě základních pracovních postupů.
- **Medplum Bots** - Napište a spouštějte logiku aplikace na straně serveru, aniž byste museli nastavovat vlastní server.
- **Knihovna komponent uživatelského rozhraní** - Komponenty React navržené tak, aby vám pomohly rychle vyvíjet vlastní aplikace pro zdravotnictví.

## Dokumenty

- Přispívání](#contributing)
  - Základní pravidla](#ground-rules)
  - [Codebase](#codebase)
    - [Technologie](#technologies)
    - [Struktura složek](#folder-structure)

## Přispívání

**Srdečně vítáme všechny příspěvky, které odpovídají našim technickým standardům!**

Jak již bylo řečeno, tato kódová základna není typickým projektem s otevřeným zdrojovým kódem, protože se nejedná o knihovnu nebo balík s
s omezeným rozsahem - je to celý náš produkt. Naše [dokumentace k příspěvkům](https://medplum.com/docs/contributing) má
všechny informace, které potřebujete, abyste mohli začít.

### Základní pravidla

#### Pokyny pro přispívání a diskusi

Poskytnutím příspěvku do tohoto projektu se má za to, že jste přijali [Developer Certificate of Origin](https://developercertificate.org/) (DCO).

Očekává se, že všechny konverzace a komunity na Medplum budou dodržovat [Community Guidelines](https://help.github.com/en/github/site-policy/github-community-guidelines) GitHubu.
a [Zásady přijatelného používání](https://help.github.com/en/github/site-policy/github-acceptable-use-policies). Očekáváme, že
že diskuse o problémech a žádostech o stažení budou pozitivní, produktivní a uctivé. Nezapomeňte: na webu jsou skuteční lidé
na druhé straně obrazovky!

#### Nahlášení chyby nebo návrh nové funkce

Pokud jste v systému Medplum našli technickou chybu nebo máte nápady na funkce, které bychom měli implementovat, je nejlepší použít nástroj pro sledování problémů.
místo, kde se s námi o ně můžete podělit. ([kliknutím zde otevřete nový problém](https://github.com/medplum/medplum/issues/new))

### Psaní dokumentace nebo obsahu blogu

Dozvěděli jste se, jak pomocí Medplum udělat něco, co nebylo zřejmé na první pokus? Přispějte svými novými znalostmi
do naší dokumentace, můžete pomoci ostatním, kteří by mohli mít podobný případ použití!

Naše dokumentace je umístěna na [medplum.com/docs](https://www.medplum.com/docs), ale je vytvořena z [Markdown](https://www.markdownguide.org/).
souborů v našem balíčku [`docs`](https://github.com/medplum/medplum/tree/main/packages/docs/docs).

Pro relativně malé změny můžete soubory upravovat přímo z webového prohlížeče na [Github.dev](https://github.dev/medplum/medplum/blob/main/packages/docs/docs/home.md).
aniž byste museli klonovat úložiště.

#### Oprava chyby nebo implementace nové funkce

Pokud najdete chybu a otevřete žádost o stažení, která ji opravuje, co nejdříve ji zkontrolujeme, abychom se ujistili, že splňuje naše technické standardy.

Pokud chcete implementovat novou funkci, otevřete nejprve problém, abyste s námi prodiskutovali, jak by funkce mohla fungovat, a zajistili, že
zapadá do našeho plánu a plánů pro aplikaci.

Pokud chcete přispět, ale nejste si jisti, jak začít, máme [štítek "good first issue"](https://github.com/medplum/medplum/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22), který se používá u issues vhodných pro nováčky. Podívejte se na [úplný seznam dobrých prvních čísel](https://github.com/medplum/medplum/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22) a vyberte si něco, co se vám líbí!

**Jste připraveni začít psát kód? ** Postupujte podle [místních pokynů k nastavení](https://www.medplum.com/docs/contributing/local-dev-setup) a vrhněte se do toho.

### Codebase Přeloženo pomocí www.DeepL.com/Translator (bezplatná verze)

#### Technologies

Když už máme základní pravidla za sebou, pojďme si říct něco o hrubé architektuře tohoto repozitáře mono:

- **Full-stack TypeScript**: Pro napájení našich serverů používáme Node.js a pro napájení našich frontendových aplikací React. Téměř všechen kód, kterého se v této kódové základně dotknete, bude v jazyce TypeScript.

Zde je seznam všech velkých technologií, které používáme:

- **PostgreSQL**: Úložiště dat
- **Redis**: Úlohy na pozadí a ukládání do mezipaměti
- **Express**: Server API
- **TypeScript**: Type-safe JavaScript
- **React**: Frontendová aplikace React

#### Struktura složek

````sh
medplum/
├── balíčky
│ ├──── agent # On-premise agent
│ ├──── app # Frontendová webová aplikace
│ ├── bot-layer # AWS Lambda Layer pro boty
│ ├──── cdk # AWS CDK infra jako kód
│ ├── cli # Rozhraní příkazového řádku
│ ├── core # Jádro sdílené knihovny
│ ├──── definitions # Definice dat
│ ├──── docs # Dokumentace
│ ├──── examples # Příkladový kód použitý v dokumentaci
│ ├── expo-polyfills # Expo polyfills for MedplumClient compatability
│ ├── fhir-router # FHIR URL router
│ ├── fhirtypes # FHIR TypeScript definitions
│ ├── generator # Code generator utilities
│ ├── graphiql # Preconfigured GraphiQL
│ ├── hl7 # HL7 client and server
│ ├── mock # Mock FHIR data for testing
│ ├── react # React component library
│ ├── react-hooks # React hooks library
│ └── server # Backend API server
└── scripts # Helper bash scripts
```

## Thanks

<a href="https://www.chromatic.com/"><img src="https://user-images.githubusercontent.com/321738/84662277-e3db4f80-af1b-11ea-88f5-91d67a5e59f6.png" width="153" height="30" alt="Chromatic" /></a>

Thanks to [Chromatic](https://www.chromatic.com/) for providing the visual testing platform that helps us review UI changes and catch visual regressions.

## License

[Apache 2.0](LICENSE.txt)

Copyright &copy; Medplum 2024

FHIR&reg; je registrovaná ochranná známka HL7.

SNOMED&reg; je registrovaná ochranná známka organizace International Health Terminology Standards Development Organisation.

LOINC&reg; je registrovaná ochranná známka společnosti Regenstrief Institute, Inc.

DICOM&reg; je registrovaná ochranná známka Národní asociace výrobců elektrických zařízení (NEMA). Přeloženo pomocí www.DeepL.com/Translator (bezplatná verze)
