# mildly-offend-me

A fortune file to midly offend. 

# prerequisites
1. You need fortune (and strfile): `brew install fortune`

Assuming you've cloned this to your home dir, simply:

1. build the file by running `./datify.sh` from the project root directory
2. link in the files to your fortune install.  The fortune file directory is the first line of output from
`fortune -f`
In my case (mac with fortune installed with homebrew)

         ln -s mildly-offend-me/mildly-offend-me $HOMEBREW_CELLAR/fortune/9708/share/games/fortunes/mildly-offend-me
         ln -s mildly-offend-me/mildly-offend-me.dat $HOMEBREW_CELLAR/fortune/9708/share/games/fortunes/mildly-offend-me.dat
3. You'll need to rebuild the binary file every time you fetch new changes.
4. You can test your fortune by typing `fortune mildly-offend-me`

# usage recommendation
add fortune to your shell's configuration to be offended every day:  
`fortune mildly-offend-me`

for extra credit, use cowsay:
```
$ brew install cowsay
$ fortune mildly-offend-me|cowsay -f stegosaurus
 _____________________________________
/ May you always get up from your     \
| computer with your headphones still |
\ attached.                           /
 -------------------------------------
\                             .       .
 \                           / `.   .' "
  \                  .---.  <    > <    >  .---.
   \                 |    \  \ - ~ ~ - /  /    |
         _____          ..-~             ~-..-~
        |     |   \~~~\.'                    `./~~~/
       ---------   \__/                        \__/
      .'  O    \     /               /       \  "
     (_____,    `._.'               |         }  \/~~~/
      `----.          /       }     |        /    \__/
            `-.      |       /      |       /      `. ,~~|
                ~-.__|      /_ - ~ ^|      /- _      `..-'
                     |     /        |     /     ~-.     `-. _  _  _
                     |_____|        |_____|         ~ - . _ _ _ _ _>
```

# pick a random cow
`brew install coreutils` is will install `gshuf`

you can then shuffle your cows:

`fortune mildly-offend-me|cowsay -f $(ls $HOMEBREW_CELLAR/cowsay/*/share/cows/*.cow | gshuf -n1)`

# colorize all the things!
for extra extra credit, pipe your fortune through lolcat! to rainbow-ify the text.

`gem install lolcat`


`fortune mildly-offend-me|cowsay -f $(ls $HOMEBREW_CELLAR/cowsay/3.03/share/cows/*.cow | gshuf -n1) | lolcat`

# Credits

 * Kevin Behrens (shamelessly stole this repo structure from him)
 * http://imgur.com//gallery/Dwj3A
