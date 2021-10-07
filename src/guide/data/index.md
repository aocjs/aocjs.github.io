# Data

This tool will allow you to parse problem's input data into an array of strings automatically. Unfortunately, retrieve input data requires a private key. This makes it harder to start using this package, but it is worth it.

## Fetch Data

This method will allow you to forget about copying by hand every input puzzle by fetching it for you. To do it, your _session_ cookie is required.


### How to retrieve your cookie

Assuming you're using Chrome, to retrieve your _session_ follow this steps:

1. Open [adventofcode.com](https://adventofcode.com).
2. Log in.
3. Open _Chrome Devtools_ (F12).
4. Go to _Application_ tab.
5. On the sidebar, under _Storage_ section, expand _Cookies_ and click on `https://adventofcode.com`.
6. Now you're seeing 3 cookies, one of them must be ***session***. Copy it's value!
7. Open your [config file](/config/) and save your cookie with key [_"session"_](/config/#session).

```json
{
  "session": "YOUR PRIVATE KEY"
}
```

## Parse data

While solving **Advent of Code** problems you will find large text files. 

```
FFBFFFBLLL
BFBFBBFRLR
FFFBFFBLLL
...
```

In the end, you will only need an array of strings with text parsed, using _newlines_ as a separator. That's what you will get on input, because that's all you need. The text file seen above, would look like this:

```json
[
  "FFBFFFBLLL",
  "BFBFBBFRLR",
  "FFFBFFBLLL",
  ...
]
```

## How AoC input data works?

**Advent of Code** allows people to compete inside webpage leaderboard. For that reason, data changes based on _session cookie_.

_Session cookie_ changes for each logged in user. But also, it changes along time, each time you log in.
