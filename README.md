# Music Library System

This is a small Python project for practicing classes, class attributes, and class methods. The main part of the project is the `Song` class in `lib/song.py`.

## What it does

Each song has three regular attributes:

- `name`
- `artist`
- `genre`

The class also keeps track of information shared by all songs:

- `count` - the total number of songs created
- `artists` - a list of unique artists
- `genres` - a list of unique genres
- `artist_count` - the number of songs for each artist
- `genre_count` - the number of songs for each genre

These values are updated automatically whenever a new `Song` object is made. For example:

```python
from song import Song

song = Song("Sicko Mode", "Travis Scott", "Rap")

print(song.name)
print(Song.count)
print(Song.artist_count)
```

The class methods used to update the shared data are `add_song_to_count`, `add_to_genres`, `add_to_artists`, `add_to_genre_count`, and `add_to_artist_count`. `add_to_artists_count` is also included as an alias for the artist count method.

## Running the project

This project uses Python and Pipenv. To install the dependencies, run:

```bash
pipenv install
```

The project can also be run with an existing Python environment that has `pytest` installed.

To run the tests:

```bash
pytest
```

Or, when using Pipenv:

```bash
pipenv run pytest
```

The sample songs at the bottom of `lib/song.py` print the current totals when the file is run or imported.

## Project layout

```text
lib/
  song.py
  testing/
    conftest.py
    song_test.py
```

The tests check that song details are saved correctly and that the shared counts, artists, and genres are updated.


