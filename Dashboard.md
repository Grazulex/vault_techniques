# 🧭 Dashboard Obsidian

Bienvenue sur ton tableau de bord personnel.

---

## 🔍 Dernières notes de veille

```dataview
table file.mtime as "Dernière modif"
from "01_TechWatch"
sort file.mtime desc
limit 5
```

---

## 🐛 Derniers bugs rencontrés

```dataview
table file.mtime as "Dernière modif"
from "02_DevNotes"
where contains(file.name, "bug")
sort file.mtime desc
limit 5
```

---

## 🏷️ Notes à relire (`#à-relire`)

```dataview
table file.mtime as "Modifiée le"
from ""
where contains(tags, "#à-relire")
sort file.mtime desc
```

---

## 📥 Inbox rapide

```dataview
list
from "00_Inbox"
sort file.mtime desc
```

---

## 📌 Projets en cours (Docs perso)

```dataview
table file.name as "Projet", file.mtime as "Dernière modif"
from "03_DocsPerso"
sort file.mtime desc
```
