  
# Finding Champions

Call the `find_champion` endpoint to 

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

A successful call returns the following JSON array. See [Champion Attributes](#champion-attributes) for details that are displayed for players:

```
champion_data = [
 {
   'name': 'ahri',
   'role':  'mid lane',
   'origin': 'vastaya'
 },
 {
   'name': 'teemo',
   'role': 'top lane',
   'origin': 'bandle city'
 },
 {
   'name':'gangplank',
   'role': 'top lane',
   'origin': 'bilgewater'
 },
 {
   'name': 'sona',
   'role': 'support',
   'origin': 'ionia'
 },
 {
   'name': 'miss fortune',
   'role': 'marksman',
   'origin': 'bilgewater'
 }
]
```

## Champion Attributes
| Attribute | Description | 
| --------- | ----------- |
| Name | The champion's name |
| Role | |
| Origin | The location within Runeterra where the champion originated |