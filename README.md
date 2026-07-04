# Kill-test landing pages — prosumer auditor & plafon tripwire

Two self-contained static pages (no external requests, no brand names, no
domains attached — per the naming rule in `leaselens/IDEAS-DECISION.md`).
Goal: measure real demand via email signups from organic Facebook-group posts
BEFORE naming or building anything.

## Files
- `prosumator.html` — "Furnizorul ți-a calculat corect factura de prosumator?"
  Form captures email + supplier (supplier mix tells us which parsers to build first).
- `plafon.html` — "Cât de aproape ești de plafonul de 100.000 €? Tu și firmele
  legate, cumulat." Form captures email + number of firms (the 2–3/4+ answers
  measure demand for the legate aggregation — the defensible feature).

## LIVE (deployed 2026-07-04, GitHub Pages)
- Prosumer: https://mihotaovidiu.github.io/landing-ro/prosumator.html
- Plafon:   https://mihotaovidiu.github.io/landing-ro/plafon.html
- Repo: https://github.com/mihotaovidiu/landing-ro (push to master redeploys)

Forms: FormSubmit → **contact@fakesp.dev** (subjects `[killtest] Prosumator…` /
`[killtest] Plafon…`, honeypot on, captcha off). **One-time activation:
FormSubmit emails an activation link on the FIRST submission — click it or
signups are silently dropped. Submit a test entry on each page NOW to trigger
it.** To change the destination email: edit the form action in both pages +
push.

Analytics: none (GitHub Pages has none) → we measure ABSOLUTE signups, per the
thresholds below. Optional: add GoatCounter/Plausible snippet later for
conversion rate.

## Facebook post copy (paste, adapt tone to the group)

### Prosumer groups (e.g. "Prosumatori România", PV-owner groups)
> Salutare! După ce mi-am verificat manual facturile de prosumator (și am găsit
> credit reportat greșit…), lucrez la o aplicație care face asta automat:
> fotografiezi factura, recalculează compensarea după noua lege și îți spune în
> 60 de secunde dacă furnizorul îți datorează bani — plus modelul de
> contestație. Nu e gata încă; vreau să văd dacă are rost s-o termin. Dacă ați
> avea nevoie de așa ceva, lăsați emailul aici: [LINK]. Ce erori ați găsit voi
> pe facturi? (curios sincer, ajută la ce verificăm întâi)

### PFA / antreprenori / contabilitate groups
> Întrebare pentru cei cu mai multe firme/PFA-uri: cum urmăriți plafonul de
> 100.000 € micro cumulat pe firmele legate? Eu n-am găsit niciun tool, doar
> Excel + panică în decembrie. Lucrez la o aplicație care arată într-un singur
> ecran cât de aproape ești — cumulat pe firmele legate — de plafonul micro și
> de cel de TVA (395.000 lei), cu alertă push înainte să le depășești. Dacă
> v-ar folosi, lăsați emailul: [LINK]. Și spuneți-mi: ce v-a prins pe picior
> greșit la plafoane anul ăsta?

Posting rules of thumb: post from the personal account, no ads, 2–3 large
groups per idea (note each group's member count), reply to every comment —
comments are qualitative signal (which errors, which suppliers, how many
firms).

## Pass / fail thresholds (decide in 7 days)
- **PASS**: ≥40 signups per idea from organic posts, or ≥8% visitor→signup if
  analytics are wired. For plafon: additionally ≥30% of signups selecting
  "2–3" or "4+" firms validates the legate wedge specifically.
- **WEAK**: 10–40 signups but rich comment engagement → iterate the claim once
  and repost in different groups before deciding.
- **FAIL**: <10 signups per idea → kill, move to the next platform vertical
  (pension / property-tax auditor) with the same template.

## After a PASS (in this order — naming rule)
1. Generate name candidates (anti-convergent, RO-rooted).
2. Verify EACH: domain available + App Store search (iTunes API, country=ro) +
   EUIPO/OSIM trademark + Google top-20.
3. Only then: buy domain, wire real emails into privacy/terms, start build
   (engine reuse from the contract-app pipeline).
