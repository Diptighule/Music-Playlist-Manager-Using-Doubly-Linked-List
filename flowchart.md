# Music Playlist Manager – Diagrams

## 1. Program Flowchart

```mermaid
flowchart TD
    A([Start]) --> B[Create Playlist]
    B --> C[Display Menu]
    C --> D[/Enter Choice/]
    D --> E{Choice}
    E -->|1| F[Add Song]
    E -->|2| G[Delete Song]
    E -->|3| H[Display Forward]
    E -->|4| I[Display Reverse]
    E -->|5| J[Play Current Song]
    E -->|6| K[Move to Next Song]
    E -->|7| L[Move to Previous Song]
    E -->|8| M[Play Complete Playlist]
    E -->|9| N[Repeat Playlist]
    E -->|10| O[Display Current Song]
    E -->|0| P([Exit])
    E -->|Other| Q[Display Invalid Choice]
    F --> C
    G --> C
    H --> C
    I --> C
    J --> C
    K --> C
    L --> C
    M --> C
    N --> C
    O --> C
    Q --> C
```

## 2. Doubly Linked List Diagram

```mermaid
flowchart LR
    NULL1((NULL)) <--> A["Song 1<br/>Title + Artist"]
    A <--> B["Song 2<br/>Title + Artist"]
    B <--> C["Song 3<br/>Title + Artist"]
    C <--> NULL2((NULL))
    H["head"] -.-> A
    T["tail"] -.-> C
    CUR["current"] -.-> B
```

Each node stores song details and two links:
- `prev` points to the previous song.
- `next` points to the next song.

## 3. Class Diagram

```mermaid
classDiagram
    class Song {
        +string title
        +string artist
        +Song* prev
        +Song* next
        +Song(string, string)
    }

    class MusicPlaylist {
        -Song* head
        -Song* tail
        -Song* current
        +isEmpty() bool
        +addSong() void
        +deleteSong() void
        +displayForward() void
        +displayReverse() void
        +playCurrent() void
        +nextSong() void
        +previousSong() void
        +playCompletePlaylist() void
        +repeatPlaylist() void
        +displayCurrent() void
    }

    MusicPlaylist --> Song : manages
```
