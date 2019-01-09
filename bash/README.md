#### links
(Bash faq)[http://mywiki.wooledge.org/BashFAQ]

#### scripts
```bash
$0 - name of the script
$n - argument of script
$# - number of arguments passed
$@ - all arguments
$? - exit status of the most recently process
$$ - process ID of the current script
```

#### variables
```bash
evn - shows all defined env variables
DIR=$(cd `dirname $0` && pwd) - current dir in script
```

