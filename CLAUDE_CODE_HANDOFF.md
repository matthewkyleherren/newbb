# Claude Code Task: Replace REKKI Text with BigBites Content

## Mission
You have a locally downloaded copy of the REKKI.com website. Your task is to systematically replace all REKKI English text with BigBites German (or Swiss German) content while preserving all HTML structure, CSS, and JavaScript functionality.

## Challenge
The same text often appears in BOTH:
- HTML files (static content)
- JavaScript files (dynamic content, strings)

You MUST replace text in both places to ensure consistency.

## Approach Strategy

### Phase 1: Analysis
1. **Scan all files** in the REKKI directory to understand structure
2. **Identify file types**: `.html`, `.js`, `.jsx`, `.ts`, `.tsx`, etc.
3. **Create a list** of all files containing text strings

### Phase 2: Text Replacement
1. **Use global search/replace** for each text mapping below
2. **Check both HTML and JS** for each string
3. **Preserve all HTML tags, CSS classes, and JS syntax**
4. **Update only the text content**, never the code structure

### Phase 3: Verification
1. **Search for "REKKI"** - should return zero results (except in comments)
2. **Search for common English words** - should mostly be gone
3. **Open in browser** and visually verify

---

## Text Replacement Mappings

### HOMEPAGE REPLACEMENTS

#### Hero Section
```
FIND: "The food wholesalers are eating their own. We're giving it back."
REPLACE (DE): "Die großen Plattformen verlangen bis zu 30%. Wir verlangen 8%."
REPLACE (CH-DE): "Die grossen Plattforme verlangid bis zu 30%. Mir chöi 8%."

FIND: "The AI-powered wholesale platform for food & drink"
REPLACE (DE): "Schweizer Antwort auf Plattformen, die denken, ein Drittel Ihres Umsatzes zu kassieren sei normal"
REPLACE (CH-DE): "De Schwiizer Antwort uf Plattforme wo denked, es Drüttel vo dim Umsatz z'kassiere sig normal"

FIND: "Get Started" (button)
REPLACE (DE): "Los geht's"
REPLACE (CH-DE): "Los geits"

FIND: "Trusted by 1,300+ suppliers globally"
REPLACE (DE): "Vertraut von 850+ Schweizer Restaurants, die rechnen können"
REPLACE (CH-DE): "Vertraut vo 850+ Schwiizer Restaurants wo nöd na rächa chönd"
```

#### Product Cards (4 sections)

**Product 1 (OrderAI → Platform)**
```
FIND: "OrderAI"
REPLACE (DE): "Plattform"
REPLACE (CH-DE): "Plattform"

FIND: "99.99% accurate AI order processing. Turn emails, voicemails, and PDFs into orders in seconds."
REPLACE (DE): "Große Plattformen verlangen 15-30% pro Bestellung. Wir 8%. Oder CHF 350 flat. Der Rest gehört Ihnen."
REPLACE (CH-DE): "Grossi Plattforme verlangid 15-30% pro Bestellung. Mir 8%. Oder CHF 350 flat. De Rest ghört dir."

FIND: "learn more" (link under OrderAI)
REPLACE (DE): "mehr erfahren"
REPLACE (CH-DE): "meh erfahre"
```

**Product 2 (InboxAI → Partners)**
```
FIND: "InboxAI"
REPLACE (DE): "Partners"
REPLACE (CH-DE): "Partners"

FIND: "AI-powered email management and customer service automation for wholesalers."
REPLACE (DE): "Nutzen Sie Uber Eats wenn's passt. Schmeißen Sie sie raus wenn nicht. Endlich Liefer-Partnerschaften, die Sie nicht besitzen."
REPLACE (CH-DE): "Bruch Uber Eats wänn's dir passt. Schmiss sie use wänn nöd. Ändlich Liefer-Partnerschäfte wo di nöd bsitzed."

FIND: "learn more" (link under InboxAI)
REPLACE (DE): "mehr erfahren"
REPLACE (CH-DE): "meh erfahre"
```

**Product 3 (MenuAI → Hardware)**
```
FIND: "MenuAI"
REPLACE (DE): "Hardware"
REPLACE (CH-DE): "Hardware"

FIND: "Analyze customer menus to identify upsell opportunities and increase order values."
REPLACE (DE): "Smarte Kiosks und Tisch-Bestellungen, die auch am Samstag Abend funktionieren."
REPLACE (CH-DE): "Smarte Kiosks und Tisch-Bestellige wo au am Samschtig Obig funktionierred."

FIND: "learn more" (link under MenuAI)
REPLACE (DE): "mehr erfahren"
REPLACE (CH-DE): "meh erfahre"
```

**Product 4 (Marketplace → Web)**
```
FIND: "Marketplace"
REPLACE (DE): "Web"
REPLACE (CH-DE): "Web"

FIND: "Zero risk customer acquisition. Pay only for orders delivered. We handle payments."
REPLACE (DE): "Websites, die Bestellungen zu Ihnen bringen, nicht zu irgendeinem Marketplace, der ewig Miete kassiert."
REPLACE (CH-DE): "Websites wo Bestellige zu dir bringed, nöd zu irgendeme Marketplace wo ewig Miet kassiert."

FIND: "learn more" (link under Marketplace)
REPLACE (DE): "mehr erfahren"
REPLACE (CH-DE): "meh erfahre"
```

#### Stats Section

```
FIND: "24,650+ hours" or similar stat
REPLACE (DE): "CHF 12'000+"
REPLACE (CH-DE): "CHF 12'000+"

FIND: "saved monthly across all customers" or similar
REPLACE (DE): "Durchschnittliche Jahreseinsparung gegenüber 25%-Plattformen (basierend auf 200 Bestellungen/Monat à CHF 35)"
REPLACE (CH-DE): "Durschnittlichi Johrseinsparig gegenüber 25%-Plattforme (basierend uf 200 Bestellige/Monat à CHF 35)"

FIND: "90%" or similar percentage
REPLACE (DE): "8%"
REPLACE (CH-DE): "8%"

FIND: "reduction in manual order processing" or similar
REPLACE (DE): "Unsere Kommission. Nicht 15%. Nicht 25%. Nicht 30%. Nicht \"hängt von Ihrer Sichtbarkeits-Stufe ab.\""
REPLACE (CH-DE): "Üsi Kommission. Nöd 15%. Nöd 25%. Nöd 30%. Nöd \"hängt vo dinere Sichtbarkeits-Stufe ab.\""

FIND: "99.99%" accuracy stat
REPLACE (DE): "99.9%"
REPLACE (CH-DE): "99.9%"

FIND: "accurate order processing" or similar
REPLACE (DE): "System-Verfügbarkeit. Weil \"Wartungsarbeiten\" während des Service inakzeptabel ist."
REPLACE (CH-DE): "System-Verfüegbarkeit. Will \"Wartungsarbet\" während em Service isch unakzeptabel."

FIND: "1,300+" suppliers stat
REPLACE (DE): "0"
REPLACE (CH-DE): "0"

FIND: "suppliers trust REKKI" or similar
REPLACE (DE): "Mal haben wir Ihre Kunden-Daten an Werber verkauft"
REPLACE (CH-DE): "Mol hämer dini Chunde-Date a Werber verkauft"
```

#### Why Choose Section (typically 4 reasons)

**Reason 1**
```
FIND: "Because we visit in person" or similar heading
REPLACE (DE): "Weil wir persönlich vorbeikommen"
REPLACE (CH-DE): "Will mir persönlich vorbi chömid"

FIND: Description about personal visits
REPLACE (DE): "Wir schicken Ihnen kein Setup-PDF und wünschen \"viel Glück\". Wir kommen in Ihr Restaurant, verstehen wie Sie arbeiten, und richten alles zusammen ein."
REPLACE (CH-DE): "Mir schicked dir keis Setup-PDF und wünscheid \"viel Glück\". Mir chömid in dis Restaurant, lueged wie du schaffsch, und richted alles zäme ii."
```

**Reason 2**
```
FIND: "Because accuracy matters" or similar
REPLACE (DE): "Weil 8% nicht 25% ist"
REPLACE (CH-DE): "Will 8% nöd 25% isch"

FIND: Description about accuracy
REPLACE (DE): "Branchen-Durchschnitt: 20-25% Kommission. BigBites: 8% flat oder CHF 350 Deckel. Der Unterschied zahlt für echte Sachen — Personal, Zutaten, Ausrüstung."
REPLACE (CH-DE): "Branchen-Durchschnitt: 20-25% Kommission. BigBites: 8% flat oder CHF 350 Deckel. De Unterschied zahlt für echti Sache — Personal, Zutate, Uusrüstig."
```

**Reason 3**
```
FIND: "Because you own your data" or similar
REPLACE (DE): "Weil Ihre Daten Ihnen gehören"
REPLACE (CH-DE): "Will dini Date dir ghöred"

FIND: Description about data ownership
REPLACE (DE): "Plattformen wissen mehr über Ihre Kunden als Sie. Das ist jetzt fertig. Jede Bestellung, jede Vorliebe, jeder Kontakt — Ihres."
REPLACE (CH-DE): "Plattforme wüssed meh über dini Chunde als du. Das isch jetzt fertig. Jedi Bestellig, jedi Vorliebe, jede Kontakt — dirs."
```

**Reason 4**
```
FIND: "Because someone needs to answer the phone" or similar
REPLACE (DE): "Weil jemand das Telefon abnehmen muss"
REPLACE (CH-DE): "Will öpper muss s'Telefon abnäh"

FIND: Description about phone support
REPLACE (DE): "Probieren Sie mal Plattform-Support am Samstag Abend zu erreichen. Oder rufen Sie uns an. Wir nehmen ab."
REPLACE (CH-DE): "Probier mal Plattform-Support am Samschtig Obig z'erreicha. Oder rüef öis a. Mir nämeds ab."
```

#### Testimonials Section

```
FIND: Testimonial section title (e.g., "What our customers say")
REPLACE (DE): "Schweizer Restaurants haben genug von Silicon Valley-Miete zahlen"
REPLACE (CH-DE): "Schwiizer Restaurants händ gnueg vo Silicon Valley-Miet zahle"

FIND: First testimonial quote (Liberty Wines or similar)
REPLACE (DE): "Wir haben 25% an Just Eat gezahlt. Das sind CHF 1'750 pro Monat für 200 Bestellungen gewesen. BigBites kostet CHF 350 flat. Mit der Ersparnis haben wir neue Küchen-Ausrüstung gekauft."
REPLACE (CH-DE): "Mir händ 25% a Just Eat zahlt. Das sind CHF 1'750 pro Monat für 200 Bestellige gsi. BigBites chostet CHF 350 flat. Mit de Ersparnis hämer neui Chuchi-Uusrüstig kauft."

FIND: First testimonial attribution
REPLACE (DE): "Picanha Brasil, Zürich"
REPLACE (CH-DE): "Picanha Brasil, Züri"

FIND: Second testimonial quote
REPLACE (DE): "Das Deckel-Modell hat alles verändert. Früher haben wir vermieden Lieferung zu bewerben weil mehr Bestellungen mehr Kosten gewesen sind. Jetzt wollen wir das Geschäft aktiv."
REPLACE (CH-DE): "S'Deckel-Modell het alles veränderet. Früener hämer vermide Lieferig z'bewärbe will meh Bestellige meh Choste gsi sind. Jetzt wänd mir s'Gschäft aktiv."

FIND: Second testimonial attribution
REPLACE (DE): "Restaurant Suvlaki, Basel"
REPLACE (CH-DE): "Restaurant Suvlaki, Basel"

FIND: Third testimonial quote
REPLACE (DE): "Große Plattformen haben 20-30% pro Bestellung gewollt. BigBites langt 8%. Wer immer noch Premium-Tarife zahlt braucht einen besseren Treuhänder."
REPLACE (CH-DE): "Grossi Plattforme händ 20-30% pro Bestellig wölled. BigBites langt 8%. Wär immer no Premium-Tariif zahlt bruucht e bessere Trühanderaber."

FIND: Third testimonial attribution
REPLACE (DE): "Fatnhappy, Luzern"
REPLACE (CH-DE): "Fatnhappy, Luzern"
```

#### Final CTA Section

```
FIND: "Stop renting. Start owning." or similar final headline
REPLACE (DE): "Hören Sie auf zu mieten. Fangen Sie an zu besitzen."
REPLACE (CH-DE): "Hör uf z'miete. Fang a z'bsitze."

FIND: Subheadline about suppliers/customers
REPLACE (DE): "Schweizer Restaurants verdienen Schweizer Lösungen"
REPLACE (CH-DE): "Schwiizer Restaurants verdiened Schwiizer Lösige"

FIND: Final CTA button
REPLACE (DE): "Los geht's"
REPLACE (CH-DE): "Los geits"

FIND: Fine print (e.g., "First month free. Cancel anytime.")
REPLACE (DE): "Erster Monat gratis. Jederzeit kündigen. Kein Vertrag. Kein Bullshit."
REPLACE (CH-DE): "Erste Monat gratis. Jederziit künde. Kei Vertrag. Ke Seich."
```

---

## Global Brand Name Replacements

### Critical: Replace ALL instances
```
FIND: "REKKI"
REPLACE: "BigBites"

FIND: "rekki"
REPLACE: "bigbites"

FIND: "Rekki"
REPLACE: "BigBites"

FIND: "@rekki"
REPLACE: "@bigbites"

FIND: "rekki.com"
REPLACE: "bigbites.ch"

FIND: "hello@rekki.com"
REPLACE: "hello@bigbites.ch"

FIND: "support@rekki.com"
REPLACE: "support@bigbites.ch"
```

---

## Navigation & Footer

### Main Navigation
```
FIND: "Product" or "Products"
REPLACE (DE): "Produkte"
REPLACE (CH-DE): "Produkt"

FIND: "About"
REPLACE (DE): "Über uns"
REPLACE (CH-DE): "Über üs"

FIND: "Pricing"
REPLACE (DE): "Preise"
REPLACE (CH-DE): "Priis"

FIND: "Contact"
REPLACE (DE): "Kontakt"
REPLACE (CH-DE): "Kontakt"

FIND: "Login" or "Sign in"
REPLACE (DE): "Anmelden"
REPLACE (CH-DE): "Aamälde"

FIND: "Get Started" (nav button)
REPLACE (DE): "Starten"
REPLACE (CH-DE): "Starte"
```

### Footer
```
FIND: "© 2024 REKKI" or similar
REPLACE: "© 2024 BigBites"

FIND: "All rights reserved"
REPLACE (DE): "Alle Rechte vorbehalten"
REPLACE (CH-DE): "Alli Rächt vorbehalte"

FIND: "Privacy Policy"
REPLACE (DE): "Datenschutz"
REPLACE (CH-DE): "Dateschutz"

FIND: "Terms of Service"
REPLACE (DE): "Nutzungsbedingungen"
REPLACE (CH-DE): "Nutzigsbedingnge"
```

---

## Meta Tags & SEO

### In <head> section of HTML files
```
FIND: <title>REKKI | ...</title>
REPLACE (DE): <title>BigBites - 8% Kommission statt 30% | Schweizer Restaurant-Plattform</title>
REPLACE (CH-DE): <title>BigBites - 8% Kommission statt 30% | Schwiizer Restaurant-Plattform</title>

FIND: <meta name="description" content="...REKKI...">
REPLACE (DE): <meta name="description" content="Die große Plattformen verlangen bis zu 30%. Wir verlangen 8%. Schweizer Restaurant-Plattform ohne Abo-Falle. 850+ Restaurants sparen durchschnittlich CHF 12'000+ jährlich.">
REPLACE (CH-DE): <meta name="description" content="Die grosse Plattforme verlangid bis zu 30%. Mir verlangid 8%. Schwiizer Restaurant-Plattform ohni Abo-Falle. 850+ Restaurants sparid durschnittlich CHF 12'000+ jährlich.">

FIND: <meta property="og:title" content="REKKI...">
REPLACE: <meta property="og:title" content="BigBites - Schweizer Restaurant-Plattform">

FIND: <meta property="og:site_name" content="REKKI">
REPLACE: <meta property="og:site_name" content="BigBites">
```

---

## JavaScript String Replacements

### Common patterns to search for in .js files:

```javascript
// Text in quotes
FIND: "The food wholesalers are eating"
FIND: 'The food wholesalers are eating'
FIND: `The food wholesalers are eating`

// Text in template literals
FIND: `${variable} - REKKI`
REPLACE: `${variable} - BigBites`

// Object properties
FIND: { title: "OrderAI", ... }
REPLACE: { title: "Plattform", ... }

// Array items
FIND: ["OrderAI", "InboxAI", "MenuAI", "Marketplace"]
REPLACE: ["Plattform", "Partners", "Hardware", "Web"]
```

---

## Step-by-Step Process for Claude Code

### Step 1: Backup
```bash
# Create backup of entire REKKI directory
cp -r /path/to/rekki-site /path/to/rekki-site-backup
```

### Step 2: Global Search
```bash
# Find all files containing "REKKI"
grep -r "REKKI" . --include="*.html" --include="*.js" --include="*.jsx" --include="*.ts" --include="*.tsx"

# Count occurrences
grep -r "REKKI" . --include="*.html" --include="*.js" | wc -l
```

### Step 3: Systematic Replacement

For EACH mapping above:

1. **Search for the English text** in all files
2. **Note which files contain it** (HTML, JS, or both)
3. **Replace in ALL locations** where found
4. **Verify replacement** by searching again (should return 0 results)

### Example workflow:
```bash
# Search
grep -r "The food wholesalers are eating" .

# Replace in HTML files (example using sed)
find . -name "*.html" -exec sed -i 's/The food wholesalers are eating their own/Die großen Plattformen verlangen bis zu 30%/g' {} +

# Replace in JS files
find . -name "*.js" -exec sed -i 's/The food wholesalers are eating their own/Die großen Plattformen verlangen bis zu 30%/g' {} +

# Verify
grep -r "The food wholesalers are eating" .  # Should return nothing
```

### Step 4: Test Locally
```bash
# Open index.html in browser
open index.html

# Or if it needs a server:
python3 -m http.server 8000
# Then visit: http://localhost:8000
```

### Step 5: Final Verification
- [ ] Search for "REKKI" → should find 0 results (except maybe in comments)
- [ ] Search for "OrderAI" → should find 0 results
- [ ] Search for "InboxAI" → should find 0 results
- [ ] Search for "MenuAI" → should find 0 results
- [ ] All German text displays correctly
- [ ] No broken JavaScript functionality
- [ ] All links still work

---

## Language Selection

**Choose ONE language for initial prototype:**

- **German (Hochdeutsch)** - Professional, widely understood
- **Swiss German** - Authentic, playful, more character

**Recommendation:** Start with **Swiss German** since it's more distinctive and matches the aggressive marketing tone better. You can always create a German version after.

---

## Important Notes

### DO:
✅ Replace ONLY text content
✅ Preserve ALL HTML tags and attributes
✅ Preserve ALL CSS classes and IDs
✅ Preserve ALL JavaScript syntax
✅ Keep ALL URLs and href values
✅ Replace in BOTH HTML and JS files
✅ Use global search/replace for consistency

### DON'T:
❌ Change HTML structure
❌ Modify CSS classes or styling
❌ Break JavaScript syntax
❌ Change file names or paths (yet)
❌ Modify image src paths
❌ Change any code logic

### Special Characters to Watch:
- Quotation marks: `"` vs `'` vs `\"`
- Escape sequences in JS: `\"`, `\'`, `\``
- HTML entities: `&nbsp;`, `&mdash;`, etc.
- Swiss characters: `ä`, `ö`, `ü`, `CHF`

---

## Testing Checklist

After replacement, verify:

- [ ] Homepage loads without errors
- [ ] All text is in German/Swiss German
- [ ] No English text remains (except maybe in comments/console)
- [ ] All buttons work
- [ ] All links work
- [ ] JavaScript animations/interactions work
- [ ] Mobile responsive design intact
- [ ] No console errors in browser developer tools

---

## If You Get Stuck

**Common issues:**

1. **Text appears in multiple formats:**
   - HTML: `<h1>Text</h1>`
   - JS string: `"Text"`
   - JS template: `` `Text` ``
   - Must replace ALL variations

2. **Special characters break:**
   - Use proper encoding (UTF-8)
   - Escape quotes in JS: `"Text with \"quotes\""`

3. **Can't find where text is:**
   - Search in ALL file types: `.html`, `.js`, `.jsx`, `.ts`, `.tsx`, `.json`
   - Check minified files: `.min.js`, `.min.css`
   - Look in data files: `.json`, `.yaml`

4. **Replacement breaks functionality:**
   - You likely replaced code, not just text
   - Restore from backup
   - Be more precise with search patterns

---

## Output Files

After completion, provide:
1. List of all files modified
2. Count of replacements made
3. Any text that couldn't be replaced (with explanation)
4. Screenshots of the prototype in browser

---

## Ready?

**Language choice:** German (DE) or Swiss German (CH-DE)?

**Directory location:** Where is your REKKI site stored?

Once you tell me, I'll provide the exact commands to run!
