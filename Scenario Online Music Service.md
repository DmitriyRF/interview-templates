# Scenario: Online Music Service

## Problem description

You are given a task to help with design and development efforts for a brand new online music service. You'll be receiving the data from a backend service, creating a class to work with a list of songs and rendering it to the client. Find the dataset description below:

| parameter_name | parameter_type | parameter_example   |
| -------------- | -------------- | ------------------- |
| title          | string         | Yesterday.mp3       |
| author         | string         | The Beatles         |
| duration       | number         | 150000 milliseconds |

*Table 1. Playlist source data example*

## Implementation details

### General questions

Let's answer some questions about class-oriented design and OOP as a whole

- What's and OOP?
- Define the core concepts of the paradigm
- What methods are called `static`?
- What methods are called `abstract`?

### Playlist  entity design

1. Create a `Playlist` class. 

   - Playlist should be able to be initialized with a list of songs as well have an ability to be initialized empty and have songs being added to it after the initialization.

2. Implement following features as class methods:

   * Retrieve a list of songs from backend

   * Store a copy of it in the local storage

   * Sort list by song duration

   * Sort list alphabetically by artist name

   * Show only songs that are performed by `artist` from a given `album`

   * Show only songs that have `._extenstion_type_` file extension (contained in the song title)

   * Show aggregate length of the playlist in seconds

   * Shuffle songs in a playlist

   * Find the song with the longest duration

   * Reverse order of songs in a playlist

   * Find the song with the longest title

   * Reverse order of words in a song's title `'one two three'->'three two one'`

   * Group files in a playlist by a given criteria

     ```javascript
     // example input
     [
       { artist: "E", title: "O" },
       { artist: "E", title: "T" },
       { artist: "B", title: "H" }
     ]
     // example output for parameter 'artist'
     ({
       E: [{ title: "O" }, { title: "T" }],
       B: [{ title: "H" }]
     });
     ```

### Designing DOM representation

You've been given a task to create a visual representation of a Playlist for the web. Starting point will be the `#container` `div` element. You need to:

   - Render an unsorted list of all the songs in the playlist. While doing so you should consider the following:
     - Each node that is going to represent a  `song` in a `Playlist` should have a `.song` class.
     - Each `song` node needs to have the following `data-*` attributes `artist,title,duration`
     - Each node should respond to a click on itself with a callback that should print a formatted message in the following way - `artist - title (duration)`

