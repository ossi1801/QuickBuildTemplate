# Use quick binds / aliases for building and running your project more efficiently
#### Use prog to create runnable functions
#### Use projenv to create project enviroment aliases (that call prog)

### prog
```bash
#!/bin/bash
build() {
  make
}
run() {
  ./main
}
case "$1" in
build | b)
  build
  exit 0
  ;;
run | r)
  run
  exit 0
  ;;
*)
  echo "Building & running project!"
  build &
  run
  exit 0
  ;;
esac
#Basic bash script "template" to increase building from commandline
#This script can be extended anyway you see fit
```
### projenv
```bash
#!/bin/bash
alias r="./prog r"
alias b="./prog b"
alias rb="./prog"
alias br="./prog"
#After creating this file
#chmod +x projenv
#source projenv
```
