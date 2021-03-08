## To setup autocomplete:
-----------*1st Method: worked for me*-------------------
 
1. Install Git and bash-completion: 
```bash
sudo apt-get install git bash-completion
```
check your git version `git --version`

2. To set your name and id
```bash
git config --global user.name "your name"
git config --global user.email "user@id.com"
```
3. restart your bash (new one)

## To Test git autocomplete
*try `git flow ` TAB shows the files under bash Or*
```bash
git chekcout master
```
this will show:
```bash
git: 'chekcout' is not a git command. See 'git --help'.

The most similar command is
        checkout
```

***That's it***

--------------------------*2nd method :(*-----------------------------
## To setup autocomplete:

- Install git `sudo apt-get install git`
- Enter the command it terminal
```bash
wget https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash
``` 
- No matter how you acquired the script, you need to rename the file to start with a period. You can do this in the terminal with this command:
```bash
mv git-completion.bash .git-completion.bash
```
Now that we have the file in your home directory with the correct filename, you need to edit either the .bash_profile or .bashrc file found also in your home directory to use the extension. Let’s use the Nano file editor to make the changes assuming you have a .bash_profile file there.
```bash
nano .bash_profile
```
In the editor window type in this code at the end of the file:
```
if [ -f ~/.git-completion.bash ]; then
   source ~/.git-completion.bash
fi
```
## Apply the changes
The script will work for all new terminal tabs (or windows), to have it running right away you need to execute it:
```bash
source ~/.bash_profile
```
*save it & exit*

## To Test git autocomplete
In new bash try `git flow ` then TAB
Or try
```bash
git chekcout master
```
this will show
```
git: 'chekcout' is not a git command. See 'git --help'.

The most similar command is
        checkout
```



