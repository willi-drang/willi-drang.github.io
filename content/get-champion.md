# Viewing Champions

Purpose of call.

Example request:

```
def find_champion(name=None, role=None, origin=None):
 champion_suggestions = []
 for champ in champion_data:
   if name:
     if champ['name'] == name:
       return [champ]
   if role:
     if champ['role'] != role:
       continue
   if origin:
     if champ['origin'] != origin:
       continue
   champion_suggestions.append(champ)
 return champion_suggestions
```

Example response:

```
def find_champion(name=None, role=None, origin=None):
 champion_suggestions = []
 for champ in champion_data:
   if name:
     if champ['name'] == name:
       return [champ]
   if role:
     if champ['role'] != role:
       continue
   if origin:
     if champ['origin'] != origin:
       continue
   champion_suggestions.append(champ)
 return champion_suggestions
```
