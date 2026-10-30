# Music Playlist Manager Using Doubly Linked List

**Assignment:** CC2 – Data Structures and Algorithms  
**Programming Language:** C++  
**Data Structure:** Doubly Linked List

## Introduction

The Music Playlist Manager is a menu-driven C++ program that manages songs using a doubly linked list. Each node stores a song title and artist, along with pointers to the previous and next nodes.

## Features

- Add a song to the playlist
- Delete a song by title
- Display songs in forward order
- Display songs in reverse order
- Play the current song
- Navigate to the next song
- Navigate to the previous song
- Play the complete playlist
- Repeat the playlist
- Display the current song

## Data Structure

Each `Song` node contains:
- `title`: song title
- `artist`: artist name
- `prev`: pointer to the previous node
- `next`: pointer to the next node

The playlist maintains:
- `head`: pointer to the first song
- `tail`: pointer to the last song
- `current`: pointer to the currently selected song

## How It Works

A doubly linked list stores songs as connected nodes. The `next` pointer moves forward, while the `prev` pointer moves backward. This allows playlist navigation in both directions.

The first song added becomes the current song. New songs are added at the end. When the current song is deleted, the next song becomes current; if there is no next song, the previous song becomes current.

## How to Compile and Run

You need a C++ compiler such as `g++`.

### Windows (PowerShell / Command Prompt)

```bash
g++ main.cpp -o music_playlist
.\music_playlist.exe
```

### Linux / macOS

```bash
g++ main.cpp -o music_playlist
./music_playlist
```

## Sample Output

```text
========== MUSIC PLAYLIST MANAGER ==========
1. Add Song
2. Delete Song
3. Display Playlist (Forward)
4. Display Playlist (Reverse)
5. Play Current Song
6. Next Song
7. Previous Song
8. Play Complete Playlist
9. Repeat Playlist
10. Display Current Song
0. Exit
Enter your choice: 1
Enter song title: Perfect
Enter artist name: Ed Sheeran
Song added successfully!

Enter your choice: 1
Enter song title: Night Changes
Enter artist name: One Direction
Song added successfully!

Enter your choice: 3

--- Playlist (Forward) ---
1. Perfect - Ed Sheeran
2. Night Changes - One Direction

Enter your choice: 5
Now Playing: Perfect - Ed Sheeran

Enter your choice: 6
Now Playing: Night Changes - One Direction

Enter your choice: 4

--- Playlist (Reverse) ---
1. Night Changes - One Direction
2. Perfect - Ed Sheeran

Enter your choice: 0
Thank you for using Music Playlist Manager!
```

*The sample output is illustrative. Your actual output depends on the songs and menu choices entered.*

## Diagrams

See [`flowchart.md`](flowchart.md) for:
1. Program flowchart
2. Doubly linked list node diagram
3. Class diagram

GitHub can render the Mermaid diagrams in the Markdown file.

## Project Files

- `main.cpp` – complete C++ source code
- `flowchart.md` – flowchart, linked-list diagram, and class diagram
- `output.txt` – sample program output
- `README.md` – project documentation

## Learning Outcomes

- Understand doubly linked lists.
- Learn node creation and pointer connections.
- Perform insertion and deletion.
- Traverse a linked list in both directions.
- Implement navigation using pointers.
- Understand dynamic memory allocation.

## Conclusion

The Music Playlist Manager demonstrates the practical implementation of a doubly linked list in C++. It allows users to add, delete, display, and navigate songs in forward and backward directions. This project provides practical understanding of dynamic memory allocation, pointer connections, node manipulation, and linked-list traversal.
