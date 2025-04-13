---
created: 2025-04-13
updated: 2025-04-13
title: 🧭 Dashboard Obsidian
---
[[todo]]
# 🧭 Dashboard Obsidian

Bienvenue sur ton tableau de bord personnel.

---

## 🔍 Dernières Notes De Veille

```dataview
table file.mtime as "Dernière modif"
from "01_TechWatch"
sort file.mtime desc
limit 5
```

---

## 🐛 Derniers Bugs Rencontrés

```dataview
table file.mtime as "Dernière modif"
from "02_DevNotes"
where contains(file.name, "bug")
sort file.mtime desc
limit 5
```

---

## 🏷️ Notes à Relire (`#à-relire`)

```dataview
table file.mtime as "Modifiée le"
from ""
where contains(tags, "#à-relire")
sort file.mtime desc
```

---

## 📥 Inbox Rapide

```dataview
list
from "00_Inbox"
sort file.mtime desc
```

---

## 📌 Projets En Cours (Docs perso)

```dataview
table file.name as "Projet", file.mtime as "Dernière modif"
from "03_DocsPerso"
sort file.mtime desc
```
