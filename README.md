# logltsv

A Handy CLI to print LTSV logs.

# SYNOPSYS

```
$ logltsv key1:value1 key2:value2 [...]
time:2014-12-10T20:55:11+0900       key1:value1     key2:value2     ...
```

# DESCRIPTION

This script prints arguments in tab-separated way, adding I<time> key-value at
the first entry of the line.

Without installing this script, you can also write an alias in your shell for
the same purpose.

Here is an example:

```sh
__logltsv() {
  echo time:$(date +%FT%H:%S:%S%z) $@ | tr -s ' ' '\t'
}
alias logltsv=__logltsv
```

# AUTHORS

YASUTAKE Kiyoshi <yasutake.kiyoshi@gmail.com>

# LICENSE

Copyright (C) 2013 YASUTAKE Kiyoshi.

This library is free software; you can redistribute it and/or modify it under
the same terms as the GNU General Public License or Artistic License.

