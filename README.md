# Tot.app addons

[Tot.app](https://tot.rocks) - An elegant, simple way to collect & edit text on your Mac, iPhone, and iPad.

## LaunchBar Actions

Copy all actions to the `~/Library/Application\ Support/LaunchBar/Actions`.

### Add to Tot

* Abbreviation: `att`
* Description: Appends text to the first Tot dot.

## Bash Script

### Installation

```shell
$ brew tap zrzka/homebrew-tap
$ brew install zrzka/homebrew-tap/tot
```

Or just copy the  `bash/tot` to the `~/bin` folder. There're no any dependencies.

### Usage

```shell
Usage: tot <dot> [ <command> ] [ <file> | - ]

<dot>:

  0|e|empty               1st EMPTY dot (can contain whitespaces)
  1|y|yellow              1st dot
  2|o|orange              2nd dot
  3|r|red                 3rd dot
  4|p|purple              4th dot
  5|b|blue                5th dot
  6|t|turquoise|c|cyan    6th dot
  7|g|green               7th dot

<command>:

  activate        select dot & activate Tot.app (default command if not provided)
  p|print         print dot contents
  a|append        append file/stdin contents to dot
  c|clear         remove dot contents
  r|replace       replace dot contents with file/stdin

<file>:

  path to a regular file (anything accepted by the cat command)
  use - for stdin (default if not provided)

Examples:

  $ tot 2                        # activate Tot.app and select second dot
  $ tot orange print             # print second dot contents to stdout
  $ tot 2 clear                  # clear contents of second dot
  $ cal -h | tot 1 append -      # append a calendar to first dot
  $ cal -h | tot 1 append        # append a calendar to first dot (fallback to stdin)
  $ tot 2 append MyApp.crash     # append a crash report to second dot
  $ tot 2 replace MyApp.crash    # replace second dot contents with a crash report
  $ tot 2 a << END               # append two lines to second dot (fallback to stdin)
  heredoc> 1st line
  heredoc> 2nd line
  heredoc> END
  ```
