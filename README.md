# Mermaid-JS-Offline
Offline Mermaid FlowChart & Diagram Maker

mermaid.min.js - https://cdn.jsdelivr.net/npm/mermaid@latest/

Put html & mermaid.min.js in a folder & open the html.

# Preview - 
![Diagram](https://github.com/Cenb9/Mermaid-JS-Offline/blob/main/Mermaid%20Diagrams%20Preview.jpg?raw=true)


🔹 Flowcharts = 

	✦ 1
```
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
	✦ 2
```
graph LR
    A[Square Rect] -- Link text --> B((Circle))
    A --> C(Round Rect)
    B --> D{Rhombus}
    C --> D
```
	✦ 3
```
flowchart TD
  A[Start] --> B{Decision}
  B -->|Option A| C[Process A]
  B -->|Option B| D[Process B]
  C --> E[End]
  D --> E
```

🔹 Pie chart = 
```
pie title What Voldemort doesn't have?
         "FRIENDS" : 2
         "FAMILY" : 3
         "NOSE" : 45
```

	✦ Pie chart (detailed) =
```
---
config:
  pie:
    textPosition: 0.5
  themeVariables:
    pieOuterStrokeWidth: "5px"
---
pie showData
    title Key elements in Product X
    "Calcium" : 42.96
    "Potassium" : 50.05
    "Magnesium" : 10.01
    "Iron" :  5
```

🔹 Gantt (horizontal bar chart) = 
```
gantt
    title Git Issues - days since last update
    dateFormat  X
    axisFormat %s

    section Issue19062
    71   : 0, 71
    section Issue19401
    36   : 0, 36
    section Issue193
    34   : 0, 34
    section Issue7441
    9    : 0, 9
    section Issue1300
    5    : 0, 5
```

🔹 Treemap (shows proportions & subcategories) = 
```
treemap-beta
"Products"
    "Electronics"
        "Phones": 50
        "Computers": 30
        "Accessories": 20
    "Clothing"
        "Men's": 40
        "Women's": 40
```

🔹 Sankey (shows flow from one set of values to another) = 
```
sankey

%% source,target,value
Electricity grid,Over generation / exports,104.453
Electricity grid,Heating and cooling - homes,113.726
Electricity grid,H2 conversion,27.14
```
	✦ 2
```
sankey

%% source,target,value
Salary, Home, 900
Salary, Living, 700
Salary, Save, 500
Home, Rent, 700
Home, Utility, 200
Living, Food, 550
Living, Transport, 150
```

🔹 Mindmap (shows hierarchy / relationships among pieces) (only SVG export) = 
```
mindmap
    root((Mind Map))
        Features
            User Management
            Order Management
            Product Management
        Architecture
            Frontend
            Backend
            Database
```

🔹 Kanban board (only SVG export) = 
```
kanban
  Todo
    [Create Documentation]
    docs[Create Blog about the new diagram]
  id10[Ready for test]
    id4[Create parsing tests]@{ ticket: MC-2038, assigned: 'K.Sveidqvist', priority: 'High' }
    id66[last item]@{ priority: 'Very Low', assigned: 'knsv' }
  id11[Done]
    id5[define getData]
    id2[Title of diagram is more than 100 chars when user duplicates diagram with 100 char]@{ ticket: MC-2036, priority: 'Very High'}
    id3[Update DB function]@{ ticket: MC-2037, assigned: knsv, priority: 'High' }
```

🔹 Class diagrams (shows the structure of a system) (only SVG export) = 

	✦ 1
```
---
title: Animal example
---
classDiagram
    note "From Duck till Zebra"
    Animal <|-- Duck
    note for Duck "can fly\ncan swim\ncan dive\ncan help in debugging"
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
        +String beakColor
        +swim()
        +quack()
    }
    class Fish{
        -int sizeInFeet
        -canEat()
    }
    class Zebra{
        +bool is_wild
        +run()
    }
```
	✦ 2
```
classDiagram
    note "This is a note for the whole diagram"
    note for Player "This is a note on the Player class"
    class GameObject {
        +String Name
        +int PosX
        +int PosY
        +Despawn() void
    }
    class DamageableObject {
        <<abstract>>
        +int MaxHealth
        -int Health
        +IsDead() bool
        +TakeDamage(int damage) void
        +OnKilled()* void
    }
    class Player {
        -int Score
        -int LivesRemaining
        +OnKilled() void
    }
    class Monster {
        -int ThreatLevel
        -Color Color
        +MakeNoise(double decibelLevel) string
        +OnKilled() void
    }
    GameObject <|-- DamageableObject
    DamageableObject <|-- Player
    DamageableObject <|-- Monster
```




✦ Open the SVG in chrome & take screenshot using Developer tools.

