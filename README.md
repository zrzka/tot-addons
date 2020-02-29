# Tot.app addons

## Bash

Copy `bash/tot` to `~/bin/tot`.

```shell
Usage: tot <dot> [ <command> ] [ <file> | - ]

Options:

  <dot>           dot number (1 to 7) or 0 as a first empty dot
  <command>       see Commands
  <file>          file path to read contents from or just - (stdin)

Commands:

  activate        select dot & activate Tot.app (default command if not provided)
  p|print         print dot contents
  a|append        append file/stdin contents to dot
  c|clear         remove dot contents
  r|replace       replace dot contents with file/stdin

Examples:

  $ tot 2                        # activate Tot.app and select second dot
  $ tot 2 print                  # print second dot contents to stdout
  $ tot 2 clear                  # clear contents of second dot
  $ cal -h | tot 1 append -      # append a calendar to first dot
  $ tot 2 append MyApp.crash     # append a crash report to second dot
  $ tot 2 replace MyApp.crash    # replace second dot contents with a crash report
  ```

  ## LaunchBar

  Copy all actions to the `~/Library/Application\ Support/LaunchBar/Actions`.

  ### Add to Tot

  * Appends text to the first Tot dot.
  