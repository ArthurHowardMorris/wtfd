# WTFD

The name stands for "What To Do", the 'F' is silent. It is minimal task
management system for folks that work in plain text environments.


## The system:

Tasks are created by writing `TODO: ` anywhere within plain text files in a
project. It is convenient,  but not required, to put these in comments. For
example:

```python 
from pandas import pd 
df = pd.read_csv('big_fat_file.csv')
# TODO: convert to a faster file format 
```

Then, from the project's root directory run `wtfd`. This creates a text file
called `todo.txt` in the root directory with the relative locations, including
line numbers, and the text of the lines, where `TODO: ` is found.

The bash script version launches an interface that allows you to select a todo item and opens your `$EDITOR` to the line where the item is found (`vim`, `nvim`, and `vscode` are supported at this time).

See `./example_the_first.md` and `./todo.txt` for an example of task creation, and the output.

## Installation:

There are two ways to set this up. You can use an alias or a bash script.

### Alias:

Recommended: 

Install the silver searcher (`brew install ag`) and bat (`brew intall bat`), then add the following alias to your `.bashrc` or `.zshrc` or `.oh-my-zsh/custom/custom_configs.zsh`.

```
alias wtfd='ag "TODO: ">todo.txt;bat todo.txt'
```

### Bash Script:

A slightly nicer, more interactive, version is provided by the bash script in this repo.
Install gum (`brew install gum`), then clone this repo, and add the folder to your path variable.

Clone this repo:
```bash 
brew install ag gum 
git clone https://github.com/ArthurHowardMorris/wtfd.git 
export PATH="$HOME/.oh-my-zsh/custom/custom_configs.zsh:$PATH"
```


