this is a file that holds some text.

it might be some writing where I describe the ways in which my todo app is the ultimate version of everything, but it does not include this at present
<!-- TODO: include this -->

The short version is:

in other todo apps, if a task arises you have two tasks

1. capture the task in your todo app 
2. do the task 

The big idea here is to minimize the following:

1. the distance between where you are when the task arises and where you record the task.
<!-- TODO: explain what this means -->
2. the distance between where the task is recorded and the context in which it needs to be addressed
<!-- TODO: explain what this means  -->
3. context switching. if you have to open your task manager you have switched contexts, if you have to decide whether the task that arose is worth switching contexts for you have already switched contexts

Related: Most 'todo list' type apps mix tasks with larger objectives and milestones. "fix this line" is captured in much the same way and place as "Write a book" and with much the same emphasis. When differentiation of the task tracking function from the project planning function, it often increases the level of disruption needed to track tasks, and the distance between the task tracking context and the task completion context. The goal of this approach is to  separates the immediate next steps and minor details of what you need to clean up from the larger planning that you do. It quickly becomes intractable to manage levels of priority and scope of different tasks, you probably shouldn't be tracking things like: confirm the definition of this variable, or fix the way this table is displayed, or 'fix this because it's ugly but it works' alongside you mile stones.

One version of this is a simple alias in your `.bashrc` or `.zshrc`

```
alias wtfd='ag "TODO: ">todo.txt;bat todo.txt'
```

this takes advantage of your directory structure to track todos in the  place where you'll use them.
and allows you to just jump directly to them (if your editor is vim or neovim or vscode)
vim and nvim are `nvim file +line_number` and vscode is `code file:line_number`

note that this could be configured to integrate with https://github.com/Swatto/td and https://mjdescy.github.io/TodoTxtMac/ and https://nerdur.com/todour-pl/ and really any similar system (though I'll have to make it work a little more)

