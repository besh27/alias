<div align="center">
    <h1>Creating an alias <h1> 
    <img alt="creating an alias" src="../assets/images/alias5.jpg"> 
</div> 

&nbsp;
## Add an alias to a profile
1. Open Terminal and type in the text below 
    - This is your "z shell" profile, which you can store aliases or nvm information. 
    - This example is for linux/macOS users, but windows users can edit their '.bash_profile' in 'C:\Users\<username>'

```zsh
    vim ~/.zshrc
```
1. Click 'i' to enter vim's input mode to start typing. Copy the code below.
   - This alias isn'tvery useful, but shows that you can shorten a command with an alias.
```zsh
    alias cl="clear"
```

3. Click the'esc' key to exit vim's input mode and type code below in the vim console. 
```zsh
    :wq!
```
4. To be able to use the new alias from your zsh profile, it will need to be "sourced". In the terminal, write the code below.

```zsh
    source ~/.zshrc
```

&nbsp;
## Alias to help create more aliases
Instead of going through the steps above, let's create some aliases to make the process easier. 

1. Enter your zsh profile once more, but this time add the code below. 
   - The re alias will re-source your profile, and the pro alias will give you quick acess to your profile


```zsh
    alias re="source ~/.zshrc"
    alias pro="vim ~/.zshrc"
```
2. Follow steps 3-4 from above to save the file and resource it. 
3. Now you will never have to write 'source /.zshrc"or 'vim /.zshrc' ever again! 
   
&nbsp;
## There's one more thing 
<div align="center">
    <img alt="creating an alias" src="../assets/images/alias6.gif"> 
</div> 

```zsh
    alias
```
- With this command you can quickly check your current alias collection. 
&nbsp;

---

BACK: [Getting started](00_getting_started.md) |
NEXT: [Creating more aliases](02_creating_more_alias.md)
