# tippitytappity-design

tippitytappity is a program to practice typing
```mermaid
classDiagram
  User <|-- Player
  Player --> TypingTest
  TypingTest --> history

  class User{
        - name: string
        - email: string
        - password: string
        + login(user: string, pass: string) boolean
  }

  class Player{
        - wpm: int
        - accuracy: flaot
        + update_stats(wpm: int, accuracy: float)
  }

  class TypingTest{
        - text: string
        - typed_text: string
        - duration_seconds: int
        + calculate_wpm() int
        + calculate_accuracy() float
  }

class history{
      - wpm: int
      - accuracy: float
      + wpm[wpm]
      + accuracy[accuracy]
}
```

## Data model

```mermaid
classDiagram
  ExampleParent <|-- ExampleChild
  class ExampleParent{
        - name: string
        - email: string
        - password: string
        + login(user: string, pass: string) boolean
        + get_email() string
  }
  class ExampleChild{
        - badges vector~string~
        + add_badge(title: string)
        + get_badges() vector~string~
  }
```
