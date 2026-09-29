# steavy.github.io

GitHub Pages-user-site van **Steavy**, gepubliceerd op <https://steavy.github.io>.

## Inhoud

- **index.md** — landing page met links naar de gepubliceerde pagina's.
- **po-scrummaster-kwaliteitscoach.md** — kopie van `docs/po-scrummaster-kwaliteitscoach.md`
  uit [Steavy/Opdrachten-in-de-markt](https://github.com/Steavy/Opdrachten-in-de-markt)
  (het wekelijks bijgewerkte detacheringsoverzicht voor kwaliteit & test, product owner en scrum master rollen).

## Pagina publiceren/updaten

De pagina is een **kopie** van het bronbestand in de opdrachten-repo. Na elke scan
die de overzichts-doc bijwerkt, de laatste versie hierheen kopiëren:

```bash
cp /root/opdrachten-in-de-markt/docs/po-scrummaster-kwaliteitscoach.md \
   /root/steavy.github.io/po-scrummaster-kwaliteitscoach.md
```

Denk aan de **Jekyll-frontmatter** bovenaan (zodat het minima-theme de pagina rendert):

```markdown
---
layout: page
title: Kwaliteitscoach, Product Owner & Scrum Master — Detacheringsoverzicht
---
```

En push daarna:

```bash
cd /root/steavy.github.io
git add -A
git commit -m "update po-scrummaster-kwaliteitscoach scan <datum>"
git push
```

> HTTPS-push faalt op deze box (geen credentials) — de remote staat op SSH
> (`git@github.com:Steavy/steavy.github.io.git`), dus `git push` werkt direct.