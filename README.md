# Känslo-tracker 💛

Känslo-tracker är en enkel webbaserad app för känslohantering, reflektion och självinsikt.  
Användaren väljer en **grundkänsla**, fördjupar den genom en **nyanserad känsla**, får **reflekterande tips** och kan spara sina insikter lokalt i webbläsaren.

Appen är skapad med fokus på:
- emotionell medvetenhet
- trygg självreflektion
- att möta känslor utan att döma eller fixa

---

## ✨ Funktioner

- Välj **grundkänsla** (ilska, rädsla, sorg, skam, glädje, avsky)
- Välj **nyans** kopplad till vald grundkänsla
- Få **slumpade, reflekterande tips**
  - prioriterar nyans-specifika tips
  - faller tillbaka på grundkänslan om nyans saknas
- Spara reflektioner och tips i **localStorage**
- Se tidigare sparad historik med datum

All data sparas lokalt – inget skickas vidare.

## 🧠 Struktur & logik

### Grundkänslor
Grundkänslor definieras i `tipsPerFeeling` och används som fallback när inga nyans-tips finns.

### Nyanser
Varje grundkänsla har sina egna nyanser definierade i objektet `nuances`.

### Tips per nyans
Mer specifika tips finns i `tipsPerNuance`, strukturerat så här:

```js
tipsPerNuance = {
  skam: {
    "dåligt samvete": [ ... ],
    skuld: [ ... ]
  },
  ilska: {
    irriterad: [ ... ]
  }
}
