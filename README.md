## Terminal Spotify Playlist
This tool allows you to populate a Spotify playlist from a CSV file.

Given a playlist name and a list of song names, it will lookup for the songs
and add them to the playlist.

Spotify WebAPI is used to communicate with the Spotify cloud.

### Usage
```
./terminal-spotify-playlist [-c <access-code>] [-t <token>] <playlist-name>
```

### Examples
In this example we add a single song to the playlist
```
echo "Yellow Submarine,Beatles" | ./terminal-spotify-playlist "Beatles"
```

In this example we read the songs from the file and add them to the playlist
```
./terminal-spotify-playlist "Beatles" < /path/to/beatles/playlist
```

### Spotify Application
To use this script you will need to create a spotify application, and
fill in the "Spotify Client ID" and the "Spotify Client Secret" in the script.

You can create an application on: https://developer.spotify.com/my-applications

When asked for redirect URIs you should fill in: http://localhost:34964
