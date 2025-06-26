---
theme: unicorn
title: AWS Gameday
class: text-center
transition: slide-left
mdc: true
layout: intro
introImage: "/gameday.png"
---


# AWS GameDay

Zabawne, grywalizowane i interaktywne doświadczenie edukacyjne.

---

# Czym jest AWS GameDay?
<v-clicks>

- 🎮 **Grywalizowane Wydarzenie Edukacyjne** - wyzwania dla uczestników do wykorzystania rozwiązań AWS w rozwiązywaniu prawdziwych problemów technicznych w zespołach
- 🚀 **Praktyczne Doświadczenie** - w pełni praktyczna możliwość dla specjalistów technicznych do eksploracji usług AWS, wzorców architektury i najlepszych praktyk
- 🔓 **Otwarty Format** - w przeciwieństwie do tradycyjnych warsztatów, GameDays nie są preskryptywne, dając uczestnikom swobodę eksploracji i kreatywnego myślenia
- 🛡️ **Bezpieczne Środowisko** - eksploruj, eksperymentuj i wprowadzaj innowacje w bezpiecznym środowisku bez obaw o awarie produkcyjne
- 👥 **Współpraca Zespołowa** - wspieranie budowania zespołu i współpracy podczas wspólnego rozwiązywania wyzwań
- 🎯 **Rzeczywiste Scenariusze** - prezentacja usług AWS przy użyciu realistycznych scenariuszy technicznych i działającej infrastruktury AWS
- 🏆 **Element Konkurencyjny** - zespoły rywalizują na tablicach wyników w czasie rzeczywistym podczas nauki i rozwiązywania wyzwań

</v-clicks>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---

# Generative AI GameDay Challenge

W ostatniej edycji pojawiło się skupienie na gen AI.
<br />Interesuje się trochę tym tematem więc pomyślałem czemu nie

<img
  v-click
  class="w-150"
  src="/why-not.jpg"
/>

---

# Jak wygląda udział w takim wydarzeniu?

<br/>

Po zapisaniu się dostałem email w którym były wszystkie informacje. <br/>
Spotkanie odbywało się na platfromie Amazon Chime <br />
Był kod wstępu i po wejściu wchodziło się na spotkanie gdzie było około 45 osób

<img class="w-100" src="/chime.png" />

---

# Wstęp i szybkie wyjaśnienie na czym będzie zabawa polegała

<br/>

Dostaliśmy szybki wstęp o tym jak to będzie wyglądało

- Praca na czas
- Zadania do zrealizowania
- Informacje podstawowe
  - Na call są pracownicy AWS, którzy będą wspierać jak ktoś utknie
  - Praca jest jednoosobowa

---
layout: table-contents
---

# Przejście do własenego pokoju oraz rozpoczęcie zabawy

<br />

Kiedy juz wszystko było wyjaśnione i upewniliśmy się, ze mamy dostep do konsoli oraz specjalnej platformy z zadaniami (Apka wyklepana i postawiona na cloudfront)

---
layout: new-section
---

# Zadanie 1 - PartyRock

---

## Czym jest PartyRock?

<div v-click.hide>

**PartyRock** to plac zabaw Amazon Bedrock do tworzenia aplikacji AI, które można udostępniać innym.

### Główne cechy:
- 🎨 **Eksperymentuj z prompt engineeringiem** - w praktyczny i zabawny sposób
- 🚀 **Buduj, udostępniaj, remiksuj** aplikacje w krótkim czasie
- 🧠 **Ucz się podstaw generative AI** - jak modele odpowiadają na prompty

### Przykłady aplikacji, które możesz stworzyć:
- Generator żartów na wybrany temat
- Tworzenie idealnej playlisty na podstawie gustu muzycznego  
- Rekomendacje posiłków na podstawie składników w lodówce
- Wirtualny quiz online ze znajomymi
- AI storyteller do kampanii RPG
</div>

<div v-after>
  <img class="w-150 absolute top-43" src="/partyrock.png" />
</div>

---
layout: new-section
---

# Zadanie 2 - Generowanie zdjęć

<style>
h1 {
  text-align: center;
}
</style>

---

<div class="absolute top-20">

# Aplikacja do generowania zdjęć w python

</div>

<div class="absolute top-40" v-click.hide>

Kolejnym zadaniem było stworzenie prostej aplikacji webowej do gen.
- Napisać prompty, które będą generowały fajne obrazki
- Oceniana była jakoś generowanych obrazków w zaleznosci od prompt

</div>

<div v-after>
  <img class="w-150 absolute top-40" src="/bedrock.png" />
</div>


---

# Ale jak to aplikacja webowa w python?

<v-click>
<img class="w-150" src="/streamlit.png" />
</v-click>

---
layout: cover-logos
logos: [
  'https://www.opc-router.de/wp-content/uploads/2023/07/Docker_150x150px-01-01-01.png',
  'https://miro.medium.com/v2/resize:fit:908/1*w4N8NNxnCo-qhADUe5BsGQ.png',
  'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT5s_irQVmNTxnN1YKjl170xsJCJg1YJys2BQ&s',
]
---

# Postawienie aplikacji

- Po zbudowaniu działającej aplikacji lokalnie trzeba było postawic kontener 
- Wypchnąć kontener na ECR
- Postawić apkę przy uzyciu ECS 
- Gotowy link do apki wrzucić do oceny


---
layout: new-section
---

# Zadanie 3 - Analiza rozmowy

<style>
h1 {
  text-align: center;
}
</style>


---

<div class="absolute top-20">

# Analiza rozmowy z konsultantem

</div>


<div class="absolute top-40" v-click.hide>

- Rozmowy są przechowywane w formacie WAV na S3
- Trzeba stworzyć transkrypcje tej rozmowy i wyciągnąć metadane

</div>

<div v-after>
  <img class="w-150 absolute top-43" src="/amazon-transcribe.png" />
</div>

---

# Stowrzenie prompta do analizy transkrycpji
<br />
Po stworzeniu transkrypcji nalezalo przejsc do bedrock studio i pokminc jak dobrze napisac prompta zeby moc mu zadawac pytania o rozmowe i zeby odpowiadal dobrze i nie wymyslal odpowiedzi i danych ktorych tam nie bylo
<br />
<br />

- Tutaj była ręczna walidacja tego czyli po testach dostawaliśmy pytania, na które sami musieliśmy odpowiedzieć uzywajac właśnie przygotowanego wcześniej AI


---
layout: image-right
image: ./guardrails.png
class: mt-35
---

# Anonimizacja danych

- Rozmowy z konsultantami zawierały wrazliwe dane takiej jak imie, nazwisko, adres, numer telefonu 

- Przed zafeedowaniem do AI mieliśmy za zadanie pozbyć się tych danych z uwagi na to, ze nie byly nam potrzebne do analizy 

---
layout: image-right
image: "https://upload.wikimedia.org/wikipedia/commons/thumb/5/5c/Amazon_Lambda_architecture_logo.svg/1200px-Amazon_Lambda_architecture_logo.svg.png"
class: mt-40
---

# Spięcie tego wszystkie w całość

Ostatecznie trzeba było połączyć wszystkie te kroki razem za pomocą lambdy

---
layout: center
---
# Inicjacja i Transkrypcja

```mermaid {theme: 'neutral', scale: 0.5}
graph LR
    A[System]
    B(S3 Bucket <br> 'raw-audio')
    C{Lambda #1 <br> 'start-transcription'}
    D[AWS Transcribe]
    E(S3 Bucket <br> 'transcriptions')
    F[Kolejny diagram na następnym slide]

    subgraph "Etap 1 i 2"
        blank1[ ]
        A -- Upload pliku .wav --> B -- s3:ObjectCreated --> C -- Uruchom zadanie --> D -- Zapisz wynik .json --> E;
    end

    E --> F;
    
    linkStyle 4 stroke-width:0px, stroke:transparent;
    linkStyle 0 stroke-width:0px, stroke:transparent;

    style B fill:#FF9900,stroke:#333
    style E fill:#FF9900,stroke:#333
    style C fill:#FF4F00,stroke:#333
    style blank1 display:none; 
```

---
layout: center
---

# Analiza, AI i Zapis

```mermaid {theme: 'neutral', scale: 0.5}
graph LR
    F{Lambda #2 <br> 'analyze-transcription'}
    G[Amazon Bedrock Guardrails]
    I((Zapisz log / Kwarantanna))
    J[Amazon Bedrock <br> Model LLM]
    K[(Baza Danych / S3 <br> 'analysis-results')]

    subgraph "Etap 3 i 4"
        F -- Wyślij tekst --> G;
        G -- "Treść OK" --> J;
        G -- "Treść Zablokowana" --> I;
        J -- Wynik analizy --> F;
        F -- Zapisz ostateczny wynik --> K;
    end
    
    linkStyle 4 stroke-width:0px, stroke:transparent;

    style F fill:#FF4F00,stroke:#333
    style G fill:#00A1F1,stroke:#333
    style J fill:#00A1F1,stroke:#333
    style I fill:#D81B1B,stroke:#333,color:#fff
```

---
layout: image-center
image: ./result.jpeg
imageWidth: '450'
imageHeight: '950'
---

# Wynik

---
layout: center
---

# Thank you!

<PoweredBySlidev mt-10 />
