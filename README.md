nytxwget
========

`nytxwget` is a New York Times crossword puzzle downloader. To use it,
place your credentials in a file named `settings.py` in the same
directory, with contents like

    login_url  = "https://myaccount.nytimes.com/auth/login"
    puzzle_url = "http://select.nytimes.com/premium/xword/"

    user       = "wshortz@nytimes.com"
    password   = "ILoveTylerHinman"

    puzzle_dir = "/srv/share/New York Times Crossword Puzzles"

Then, run it like

    ./nytxwget 2012-01-01 2012-01-31

to get puzzles in both PUZ and PDF formats for the specified range of
dates. They'll be downloaded to the directory you specify with
`puzzle_dir` in `puz/` and `pdf/` subdirectories which themselves have
subdirectories for each day of the week and for the last 14 days'
puzzles.
