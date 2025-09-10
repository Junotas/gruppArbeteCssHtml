# Förklaring av Koden - Planned Planthood - Grupp 5

## Projektöversikt

Detta projekt är en webbplats för trädgårdsplanering som hjälper användare att organisera sina planteringar i kolonilotter. Webbplatsen består av två sidor: en startsida och en användardashboard.

## Uppfyllda Krav

### Semantisk HTML
**Krav:** Använda semantiska HTML-element och max 2 div-element per sida.

**Vad vi gjorde:**
- Använde `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>` istället för div-element
- Ersatte div-element med `<figure>` för bilder, `<ul>/<li>` för listor, och `<section>` för innehållsgrupper
- Endast 2 div-element kvar per sida för nödvändiga behållare

**Varför:** Semantiska element gör koden lättare att förstå och förbättrar tillgängligheten för skärmläsare.

### Responsiv Design
**Krav:** Minst 2 brytpunkter som fungerar på desktop och mobil.

**Vad vi gjorde:**
- Mobile-first approach med brytpunkter vid 768px och 480px
- Använde `clamp()` för responsiv typografi
- Flexibla layouter som anpassar sig till olika skärmstorlekar

**Varför:** Användare ska kunna använda webbplatsen på alla enheter med samma bra upplevelse.

### CSS Layout-metoder
**Krav:** Minst ett område med CSS Grid och ett med Flexbox.

**Vad vi gjorde:**
- **CSS Grid:** För hero-sektion, funktionsgrid, galleri och dashboard
- **Flexbox:** För navigation, kortinnehåll och knappgrupper

**Varför:** Grid är perfekt för tvådimensionella layouter, Flexbox för endimensionella. Olika verktyg för olika behov.

### BEM Namngivning
**Krav:** Konsekvent BEM-namngivning genom hela projektet.

**Vad vi gjorde:**
- Använde Block__Element--Modifier struktur
- Exempel: `.nav__logo`, `.hero__button`, `.feature-card__title`

**Varför:** BEM gör koden självförklarande och förhindrar CSS-konflikter.

### Tillgänglighet
**Krav:** Alt-texter för alla bilder.

**Vad vi gjorde:**
- Beskrivande alt-texter på svenska för alla bilder
- Fokus-stilar för tangentbordsnavigation
- Stöd för högkontrast och reducerad rörelse

**Varför:** Webbplatsen ska fungera för alla användare, inklusive personer med funktionsnedsättning.

## Tekniska Beslut

### Varför Mobile-First?
Började med mobil-design och byggde uppåt. Det ger bättre prestanda och säkerställer att mobila användare får den bästa upplevelsen.

### Varför clamp() för Typografi?
`clamp()` gör texten flytande responsiv. Minimum 1.5rem, föredragen 4vw, maximum 2.5rem. Bättre än media queries för text eftersom det skalas smidigt.

### Varför Separata CSS-filer?
Skapade `index.css` för delade stilar och `mina.css` för sidospecifika stilar. Det gör koden mer organiserad och lättare att underhålla.

### Varför Semantiska Element?
Istället för div-element använde vi:
- `<figure>` för bilder med beskrivningar
- `<ul>/<li>` för listor av objekt
- `<section>` för innehållsgrupper
- `<article>` för oberoende innehåll

Detta gör koden mer meningsfull och förbättrar tillgängligheten.

## Struktur

### index.html (Startsida)
- Hero-sektion med huvudbudskap
- Funktionskort som förklarar fördelar
- Galleri med inspirerande bilder
- Call-to-action för att uppmuntra användning

### mina.html (Användardashboard)
- Dashboard med statistik över planteringar
- Lista över användarens planteringar med status
- Kalender-sektion för planering

### index.css (Delade Stilar)
- Grundstilar och typografi
- Navigation och footer
- Responsiva brytpunkter
- Tillgänglighetsfunktioner

### mina.css (Sidospesifika Stilar)
- Dashboard och statistik-kort
- Planteringskort med status
- Kalender-sektion
- Sidospecifika responsiva regler

## Färgschema

- **Mörkgrön (#2c5530):** Rubriker och viktig text
- **Mellangrön (#4a7c59):** Knappar och länkar
- **Ljusgrön (#e8f5e8):** Bakgrunder
- **Vit (#ffffff):** Kort och sektioner
- **Grå (#666):** Mindre viktig text

## Responsiva Brytpunkter

- **Desktop (1200px+):** Tvåkolumnslayout, stora bilder
- **Surfplatta (768px-1199px):** Enkelkolumnslayout, medelstora bilder
- **Mobil (480px-767px):** Staplad layout, små bilder
- **Liten mobil (<480px):** Minimal padding, komprimerat mellanrum

## Prestanda

- Använde AVIF-format för bilder (modern komprimering)
- En CSS-fil för delade stilar (färre HTTP-begäranden)
- Effektiva CSS-selektorer
- Hardware-acceleration för animationer

## Slutsats

Webbplatsen uppfyller alla krav från uppgiften och använder moderna webbutvecklingspraxis. Koden är organiserad, tillgänglig och responsiv, vilket ger användarna en bra upplevelse på alla enheter.
