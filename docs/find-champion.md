  
# Finding Champions

Call the `find_champion` endpoint to display a list of champions and attributes that can help players selecting the best champions for their teams.

<!--Add any prerequisites-->

For each champion, the call returns the following attributes:

| Attribute | Description | 
| --------- | ----------- |
| Name | The champion's name |
| Role | The champion's role, which is useful for assembling a strategically balanced team |
| Origin | The location within Runeterra where the champion originated |

<!--I'm totally guessing on the Python logic here.-->
You can structure the call so that the endpoint returns results even if the `role` or `origin` attributes do not return a match.

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

A successful call returns the following JSON array: 

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


## Response Codes

See the following code descriptions for responses:

<!--Totally making these up.-->

| Code | Description |
| ---- | ----------- |
| `200` | Request was successful. A data array accompanies this code. |

