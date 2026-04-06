```markdown
# Sequence Diagram

```plantuml
@startuml
actor "Лиса" as Fox
participant "Теремок" as H
participant "Мышка" as Mouse

Fox -> H : запроситьВход()
activate H
H -> Mouse : Кто живёт?
Mouse --> H : Я
H -> H : проверить вес
H -> Fox : разрешить вход
deactivate H
@enduml
