# goodreadsh
Command line interface for [Goodreads](https://goodreads.com).

## Installation

1. Download the `goodreads` executable.
    1. Clone this repository.
    2. Grant executable permission to `goodreads`
    3. Add directory path to `PATH`
```sh
$ git clone https://github.com/prakashdanish/goodreadsh && cd goodreadsh
$ export PATH="$PATH:/path/to/dir"
$ chmod +x goodreads
```

#### Developer key
`goodreadsh` requires a goodreads developer key in order to use it's API. Generating your developer key is easy.
1. Access your developer key [here](https://www.goodreads.com/api/keys).
2. Copy your developer key over to `goodreadsh`'s config file. `~/.goodreads.conf`
```sh
DEVELOPER_KEY="<your_key_here>"
```

## Usage
```sh
=========
goodreads
=========

Usage: 
  goodreads [option]

Options:
  book:     book related options
  author:   author related options
  user:     user related options


====
book
====

Usage:
  goodreads book [--option] [title]

Options:
  -r --rating:        show average rating
  -R --rating-dist:   show rating distribution
  -a --author:        show author name
  -d --desc:          show book description
  -g --id:            show goodreads id


======
author
======

Usage:
  goodreads author [--option] [name]

Options:
  -b --books:         show top books by author
  -B --all-books:     show all books by author
  -a --about:         show about author
  -i --info:          show author info
  -g --id:            show goodreads id


====
user
====

Usage:
  goodreads user [--option] [username|id]

Options:
  -a --about:             show user info
  -g --id:                show goodreads id
  -s --shelf [label]:     show top books by author
```
