# music-data-governance
Pipeline that maps user's Spotify data with MusicBrainz.
The data is stored in a datalake.

## Setup project

1. Create and source virtual env

```bash
python -m venv .venv
source .venv/Scripts/activate
```

2. Create scaffold

```bash
touch Makefile && touch requirements.txt
```

3. Populate Makefile

```bash
install:
    pip install --upgrade pip &&\\
        pip install -r requirements.txt

test:
    python -m pytest -vv --cov=hello --cov=hellocli test_hello.py

lint:
    pylint --disable==R,C hello.py hellocli.py

all: install lint test
```