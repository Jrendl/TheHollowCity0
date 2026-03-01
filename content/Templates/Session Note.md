---
{"publish":true,"permalink":"/Templates/Session Note.md","created":"2026-01-11T14:25:39.407-06:00","modified":"2025-12-08T01:31:00.000-06:00","published":"2025-12-08T01:31:00.000-06:00","tags":["SessionNote"],"cssclasses":"","sessionNum":"undefined","summary":null,"Date":"<% tp.date.now(\"dddd, MMMM Do, YYYY\") %>"}
---

# [[<%tp.file.title%>]]
---
*Session Number*: `VIEW[<%tp.file.title.split(" ")[1]%>][math:sessionNum]`
`INPUT[textArea:summary]`
`BUTTON[newNpc]`    `BUTTON[newDay]`
## Notes

<%tp.file.include("[[Templates/In Game Day]]")%>
