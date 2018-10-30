# BFuzz
[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)
```
BFuzz is currently in beta. 
```

BFuzz is an input based fuzzer tool which take `.html` as an input, open's up your browser with a new instance and pass multiple testcases generated by domato which is present in `recurve` folder of BFuzz, more over BFuzz is an automation which performs same task repeatedly.

## Run BFuzz

```
warmachine@ftw:~/BFuzz$ ./generate.sh
warmachine@ftw:~/BFuzz$ python BFuzz.py 
Enter the browser type:
 1: Chrome 
 2: Firefox
>>
```
Running `python BFuzz.py` will ask for option weather to fuzz Chrome or Firefox, however if selected `2` this will open firefox `firefox --new-instance` and randomly open any of the testcase from `recurve` create the logs on the terminal wait for `3 seconds` again it will open firefox and the same process continue so on.

BFuzz is a small `.py` script which enable's to open browser run testcase for `12 seconds` then close wait for `3 seconds` and again follow the same process.

## Domato 🍅
The testcase's in `recurve` are generated by [domato](https://github.com/googleprojectzero/domato)
generator.py contains the main script. It uses grammar.py as a library and contains additional helper code for DOM fuzzing.

grammar.py contains the generation engine that is mostly application-agnostic and can thus be used in other (i.e. non-DOM) generation-based fuzzers. As it can be used as a library, its usage is described in a separate section below.

.txt files contain grammar definitions. There are 3 main files, html.txt, css.txt and js.txt which contain HTML, CSS and JavaScript grammars, respectively. These root grammar files may include content from other files.

## Bug showcase
Epiphany Web 3.28.1: [CVE-2018-11396](https://bugzilla.gnome.org/show_bug.cgi?id=795740)<br>
Mozilla Firefox: Stack based buffer overflow bug ID: 1456083 [Went DUPLICATE] <br>

## View in action
[Browser Fuzzing via BFuzz](https://youtu.be/I59SkL0ReUM)

## Contribution

Please feel free to PR.

## ToDo

Handle Exeception, Add banner, Optimize Code, Mangle testcases.

