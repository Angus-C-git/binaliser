# binaliser

A **basic** binary diagnostics tool/analyser for ELF binaries.

## Usage

`./binaliser <binary> [options]`

## 'Features'

+ Make guesses about exploitation tactics and strategies
+ Determine offsets for return pointer in simple buffer overflows
+ Determine buffer offsets for format string exploits in simple binaries


## Known Issues

+ Ubuntu and probably other distros don't always dump a core file after a segfault occurs
+ This will cause the automatic bof offset calculation to fail
  + Sometimes `ulimit -c unlimited` can fix this
+ If the vulnerable input field is indirect (not the first input from stdin on run) then the auto fuzzer will fail
  + Support for indirect input fuzzing is a TODO