#### links
[bash faq](http://mywiki.wooledge.org/BashFAQ)

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

#### flags
```
set -x debug mode
set -e automatic error detection, not recommended
```

#### one line
```
for i in {1..10}; do; echo $i; done                             - one line loop
if [[ $filename = *.jpg ]]; then; echo "$filename is jpg"; fi.  - checking filename pattern 
```
