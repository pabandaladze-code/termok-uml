```markdown
# Class Diagram

```plantuml
@startuml
skinparam classAttributeIconSize 0

class Теремок {
  - maxWeight: int
  - currentOccupants: int
  - totalWeight: int
  + добавитьЗверя(зверь: Зверь): bool
  + разрушить(): void
}

abstract class Зверь {
  - имя: String
  - вес: int
  + запроситьВход(теремок: Теремок): void
}

class Мышка extends Зверь
class Лягушка extends Зверь
class Зайчик extends Зверь
class Лисичка extends Зверь
class Волчок extends Зверь
class Медведь extends Зверь

Теремок "1" o-- "*" Зверь : содержит
Зверь <|-- Мышка
Зверь <|-- Лягушка
Зверь <|-- Зайчик
Зверь <|-- Лисичка
Зверь <|-- Волчок
Зверь <|-- Медведь

note top of Теремок : Максимальный вес = 100
note bottom of Медведь : Игнорирует вес, разрушает теремок
@enduml
