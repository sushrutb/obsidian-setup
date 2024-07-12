---
created: <% tp.file.creation_date() %>
---
# <% moment(tp.file.title,'YYYY-MMM-DD').format("dddd, MMMM DD, YYYY") %>

<< [[Daily-Notes/<% tp.date.now("YYYY", -1) %>/<% tp.date.now("MMMM", -1) %>/<% tp.date.now("YYYY-MMM-DD", -1) %>|Yesterday]] | [[Daily-Notes/<% tp.date.now("YYYY", 1) %>/<% tp.date.now("MMMM", 1) %>/<% tp.date.now("YYYY-MMM-DD", 1) %>|Tomorrow]] >>


---
# Journal

How did you sleep?

How are you feeling?

Are you making progress?

What do you want to achieve today?

What is the main thing you want to think about and make a decision on?

---

# Habits

- [ ] Journal ⏫ 
- [ ] Exercise ⏫ 
- [ ] Work on project⏫ 
- [ ] Learn🔼 

---

# Task Log

```tasks
done on {{date:YYYY-MM-DD}}
```


---
# 📝 Notes


#### Notes created today

```dataview
Table dateformat(file.ctime, "yyyy-MM-dd HH:mm") AS "Last Modified" FROM "" AND -"Daily Notes" WHERE file.ctime.day = this.file.ctime.day AND file.ctime.month = this.file.ctime.month SORT file.ctime desc
```

#### Notes last touched today

```dataview
Table dateformat(file.mtime, "yyyy-MM-dd HH:mm") AS "Last Modified" FROM "" AND -"Daily Notes" WHERE file.mtime.day = this.file.ctime.day AND file.mtime.month = this.file.mtime.month SORT file.mtime desc
```
