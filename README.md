<h1 align="center">goodreadsh</h1>
<p align="center">Command line interface for <a href="https://goodreads.com" > Goodreads</a></p>
<p align="center">
<a href="https://i.imgur.com/der2fH7.gif"><img src="https://i.imgur.com/der2fH7.gif" width="600"/></a>
</p>

## Installation

#### Homebrew
Easiest way to install on macOS is by using [Homebrew](https://brew.sh).

```console
$ brew tap prakashdanish/homebrew-formulae
$ brew install goodreadsh
```

#### Manual installation
1. Clone this repository.
2. Grant executable permission to `goodreads`
3. Add directory path to `PATH`
```console
$ git clone https://github.com/prakashdanish/goodreadsh && cd goodreadsh
$ export PATH="$PATH:/path/to/dir"
$ chmod +x goodreads
```

#### Developer key
`goodreadsh` requires your developer key in order to use the goodreads API, obtaining one is fairly trivial.

1. Access your developer key [here](https://www.goodreads.com/api/keys).
2. Copy your developer key over to `goodreadsh`'s config file. `~/.goodreads.conf`
```sh
DEVELOPER_KEY="<your_key_here>"
```
Your config file should already be present in your home dir `~/.goodreads.conf` and if it's not, then run the command once without any options or create the file manually.

## Usage

```text
=========
goodreads
=========

Usage: 
  goodreads [option]

Options:
  book:     book related options
  author:   author related options
  user:     user related options
  help:     show help message



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
  -s --shelf [label]:     show books from given shelf
```

## Examples

```sh
$ goodreads book --rating 1984
4.16

$ goodreads book --rating-dist "animal farm"
★ ★ ★ ★ ★ : 736953
★ ★ ★ ★ ☆ : 768149
★ ★ ★ ☆ ☆ : 463984
★ ★ ☆ ☆ ☆ : 143183
★ ☆ ☆ ☆ ☆ : 71234

Total : 2183503

$ goodreads author --books orwell
1984
Animal Farm
Animal Farm / 1984
Down and Out in Paris and London
Homage to Catalonia
Burmese Days
Keep the Aspidistra Flying
The Road to Wigan Pier
Coming Up for Air
Shooting an Elephant

$ goodreads user --shelf currently-reading prakashdanish
Learn Vimscript the Hard Way
The Linux Command Line
Norwegian Wood
Practical Vim: Edit Text at the Speed of Thought

$ goodreads book --desc "my experiments with truth"
Mohandas K. Gandhi is one of the most inspiring figures of our time. In his classic....<snipped>

```
## Contribution
If you would like to contribute, submit an issue and/or send a PR.

## License
MIT License

Copyright (c) 2018 [Danish Prakash](https://github.com/prakashdanish)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
