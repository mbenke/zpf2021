## Materiały do wykładu "Zaawansowane Programowanie Funkcyjne" Wydział MIM UW 2020/21

## "Advanced Functional Programming" course materials, MIMUW 2020/21

* Generated Lecture notes in the www subdir, source in Slides
* Generating lecture notes and slides needs pandoc

### Quick start

~~~~~
$ cabal update
$ cabal install pandoc
$ PATH=~/.cabal/bin:$PATH            # Linux
$ PATH=~/Library/Haskell/bin:$PATH   # OS X
$ git clone git://github.com/mbenke/zpf2021.git
$ cd zpf2021/Slides
$ make
~~~~~

or using stack - https://haskellstack.org/

~~~~
stack setup
stack install pandoc
export PATH=$(stack path --local-bin):$PATH
...
~~~~

On students, you can try using system GHC:

~~~~
export STACK="/home/students/inf/PUBLIC/MRJP/Stack/stack --system-ghc --resolver lts-12.26"
$STACK setup
$STACK config set system-ghc --global true
$STACK config set resolver lts-12.26
$STACK upgrade --force-download  # or cp stack executable to your path
#  ...
#  Should I try to perform the file copy using sudo? This may fail
#  Try using sudo? (y/n) n

export PATH=$($STACK path --local-bin):$PATH
stack install pandoc
~~~~

Installing `pandoc` is optional, there are prebuilt HTML files in the `www` folder (or you can just read markdown).
