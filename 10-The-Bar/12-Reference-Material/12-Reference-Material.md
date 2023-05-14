---
attribution: Craftidore
creation: 2023-05-14
modified: 2023-05-14
type: folder
---

# `=this.file.name`

This folder is for things that are referenced in the [[20-Bathroom-Library]], and need a note of explanation, but aren't really part of the [[20-Bathroom-Library]] itself.
For example, notes on RPG systems go here, as do broad concepts ('what's a BBEG?').
Additionally, any verbatim content (like SlyFlourishes' Creative Commons 4 material) goes here.

```dataview
TABLE author AS Author, link AS Link 
FROM "10-The-Bar/12-Reference-Material" 
WHERE this.file.name != file.name
SORT file.name ASC
```
