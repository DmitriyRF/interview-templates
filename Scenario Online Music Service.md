# Scenario: Online Music Service

## Task description

You are given a task to help with design and development efforts for a brand new online music service. You'll be tasked with the following activities:

1. Design a simple UI that should contain:

   * Playlist
   * Control area

   - File info

2. Create a `Playlist` class.

3. Implement following features as class methods:

   * Retrieve a list of songs from backend

   * Store a copy of it in the local storage

   * Sort list by song duration

   * Sort list alphabetically by artist name

   * Show only songs that are performed by `artist` from a given `album`

   * Show only songs that have `._extenstion_type_` file extension

   * Show aggregate length of the playlist in seconds

   * Shuffle songs in a playlist

   * Find the song with the longest duration

   * Reverse order of songs in a playlist

   * Find the song with the longest title

   * Group files in a playlist by a given criteria

     ```javascript
     // example input
     [
       { artist: "E", title: "O" },
       { artist: "E", title: "T" },
       { artist: "B", title: "H" }
     ]
     // example output
     ({
       E: [{ title: "O" }, { title: "T" }],
       B: [{ title: "" }]
     });
     ```