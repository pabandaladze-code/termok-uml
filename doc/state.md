```markdown
# State Diagram

```plantuml
@startuml
[*] --> Empty
Empty --> Occupied : заселение
Occupied --> Full : лимит веса
Empty --> Destroyed : Медведь
Occupied --> Destroyed : Медведь
Full --> Destroyed : Медведь
Destroyed --> [*]
@enduml
