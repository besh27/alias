<div align="center">
    <h1>Creating more aliases<h1> 
    <img alt="creating an alias" src="../assets/images/alias2.jpg"> 
</div> 

&nbsp;
## Alias syntax and options 
```zsh 
    alias name=value 
    alias name='command alias' 
    alias name='command arg1 arg2'
    alias name='/path/to/script' 
    alias name='/path/to/script arg1' 
```

&nbsp;
## List of alias tools
| Command | Explanation |
|---------|-------------|
| <code> alias cl="clear" </code> | clear shorthand alias |
| <code> alias l="ls -la"</code> | ls -la shorthand alias|
| <code> alias b="cd ..; l"</code> | cd to parent directory|
| <code> alias bb="cd ../..; l"</code> | cd to grandparent direcory|
| <code> alias rmdir='rm -R'</code> | rm -R shorthand |
| <code> alias see='cat -n'</code> | view file in commandline |
| <code> alias mongodb='~/mongodb/bin/mongod --dbpath ~/Documents/data/db'</code> | connect to mongo |
| <code> alias running='ps wuax | grep mongo'</code> | view current running mongodb's|

&nbsp;
## List of aliases that get you places!
| Command | Explanation |
|---------|-------------|
| <code> alias d="clear; cd ~/Documents && pwd && l"</code> | Navigate to Documents directory |
| <code> alias a="clear; cd ~/Documents/apps && pwd && l"</code> | Navigate to apps directory |
| <code> alias c="clear; cd ~/Documents/classes && pwd && l"</code> | Navigate to classes directory|
| <code> alias r="clear; cd ~/Documents/../../.. && pwd && l"</code> | Navigate to root directory |

&nbsp;
## Built in reference aliases
| Command | Explanation |
|---------|-------------|
| <code> alias re="source ~/.bash_profile"</code> | resource profle |
| <code> alias pro="vim ~/.bash_profile"</code> | view profile via VIM |
| <code> alias globals='npm list -g --depth=0'</code> |view current npm globals installed |
| <code> alias shells='cat /etc/shells'</code> | view current shells installed |
| <code> alias ref="perldoc perlreref"</code> | view a perl / regex ref|
| <code> alias chelp="vim ~/.bash_help"</code> | bash manual |
| <code> alias retropi="ssh pi@ipaddress"</code> | random retropie SSH |
| <code> alias notes="vim ~/.notes"</code> | View personal notes|
| <code> alias dosbox="vim ~/Library/Preferences/DOSBox\ 0.74-3\ Preferences"</code> | View dosbox ref|

&nbsp;
## Alias functions examples
```zsh
search() { history | grep -c $1; history | grep $1;}
count() { history | grep -c $1;}
ch() { cd "$@" && pwd && l; }

develop(){
if [ -d "$1" ];
then
   echo "File $1 exists and will be opened in VSCode. Enjoy!";
   cd $1;
   code .;
else
   echo "Creating new the directory $1 and opening it in VSCode. Enjoy!" >&2
   mkdir $1;
   cd $1;
   npm init -y;
   mkdir src && mkdir public;
   code;
fi
}

```

---

BACK: [Creating an alias](01_creating_an_alias.md) | 
NEXT: [Alias resources](03_resources)
