# git-credits

[![Build Status][ci-badge]][travis]
[![Coverage][codecov-badge]][codecov]
[![bitHound Overall Score][bithound-badge]][bithound]

Print list of contributors.


## Usage

Using [git-changelog] and [hub] you can create a list of change for a new release, append

```
git changelog v1.0.1 > draft.md
git credits v1.0.1 >> draft.md
hub release create --draft --file=draft.md --browse v1.1.0
```

By default, maintainers are excluded from the credits. `git-credits` will look them up from "package.json", MAINTAINERS.md, from the file define with the `--config` flags or from git config:

```
git config credits.maintainers --add "Damien Lebrun <damien@example.com>"
```


## Installation

```
npm install -g git-credits
```


## License

MIT License

Copyright (c) 2017 Damien Lebrun


[travis]: https://travis-ci.org/dinoboff/git-credits
[ci-badge]: https://travis-ci.org/dinoboff/git-credits.svg?branch=master
[bithound]: https://www.bithound.io/github/dinoboff/git-credits
[bithound-badge]: https://www.bithound.io/github/dinoboff/git-credits/badges/score.svg
[codecov]: https://codecov.io/gh/dinoboff/git-credits
[codecov-badge]: https://codecov.io/gh/dinoboff/git-credits/branch/master/graph/badge.svg
