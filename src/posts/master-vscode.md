---
title: 5 Key Areas To Master VSCode
date: 2021-02-23T14:02:53.585Z
tags:
  - blog
---
VSCode has become the hot tool in development. We don't all have to like it, but you can't deny it is the most used development tool with over [50% of developers using it for their daily work.](https://insights.stackoverflow.com/survey/2019#development-environments-and-tools)

The flexibility of VSCode is what makes it such a solid tool for various forms of development. Out of the box, it's a super simple text editor. There is never a reason to use any of its fancy tooling or community created extensions, however, if you really want to make the most of VSCode here are the 5 key areas you need to understand.

**\*Disclaimer!!\****: Most of the shortcuts will state **Cmd**, kindly translate this to **Ctrl** if you use a non-MacOS related device.* 

## Navigation

This editor is FULL of keyboard shortcuts, a lot of them come in handy for traversing the crazy number of tabs we mindlessly open up. 

**`Cmd + P`**: Quickly Jump to File

If you don't know of this one already it's a superpower! You don't even have to be great at spelling, VSCode is really good at shortlisting the possible file(s) you may be looking for.

![](/images/jump_to_file.gif)

Another great way to traverse around without having the file explorer open is the top path bar; it's a hidden gem I recently learned about. You can click on the file or folder in the path, and it expands to let you pick any file sitting beside it. Check it out:

![](/images/path_bar.gif)

Since VSCode is based on Electron, you use the tab switching shortcut from Chrome + Terminal + Firefox... basically most applications that have tabs.

**`Cmd + Shift + [ or ]`**: Go to Left or Right Tab

![](/images/tab_shifting.gif)

## Intellisense

Intellisense is my favourite component to VSCode, it's so seamless. VSCode gives you very basic static analysis and refactoring capabilities depending on the type of file you're editing.

**`Ctrl + Space`**: Activate autocomplete feature for item under cursor

![](/images/autocomplete.gif)

The editor also showcases all of the properties, methods, and blocks of the current file in the `Outline` window (Bottom-Left). This can be opened from the Command Palette we used previously to navigate by simply entering `@`. You can use the Command Palette like this to navigate within your active file with either `@` or `:`. 

![](/images/jump_to_section.gif)

The real meat of intellisense comes in it's refactoring capabilities! I will showcase my most used feature and leave the rest for you to explore. Did you know you can rename a variable safely across your whole codebase? 

![](/images/rename.gif)

I was only able to show an example from a local function in my project. Try it in your own codebase, it will affect the naming for all appropriate instances.

## VCS/Git

I like using the command line for Git personally, on the other hand a lot of my co-workers say a GUI Git tool is the best.

![](/images/whatever.gif)

Whichever option you choose, the out-of-the-box VCS and Git feature is useful. It's so powerful with diff-checking, conflicts, tracking by file, etc.... For command line users, this can be a time-saver. For GUI users, this means one less application to open and have running on your machine. To me, this is a win/win.

You can access the VCS window on the left-hand side (it looks like the Git logo). It's pretty difficult to cover everything it has to offer without adding a million images, but the big thing to note are the vertical ellipsis and the quick options when hovering over a file.

![](/images/VCS.png)

Refined and common Git commands can be accessed by clicking the ellipsis. The **plus** lets you add all changes to the next commit, whilst the **hooked arrow** lets you rollback all changes. When you click on a file, the diff will be shown in the main window as a split between old and new. Get used to checking this tab and running through your files before committing!! It has saved me from minor mistakes and endless build times on multiple occasions.

![](/images/diff.png)

Now if only there was a way to review PRs in VSCode when using Github enterprise. If any of you know of a tool like this, please DM me on [Twitter](https://twitter.com/talesofadev) 🙏

## Zen Mode

Let your mind be free of distractions 📿 

**Cmd + K -> Z**

*If you can use this mode effectively, you know you have mastered VSCode*

## Extensions

I think we all know about Extensions, they are essentially plugins to help with specific issues/expansions you want for the editor. As a web developer I use a few productivity and tracking extensions:

* Todo Tree
* Todo Highlight
* Prettier
* GitLens
* Language-specific extensions
* Bonus: Themes