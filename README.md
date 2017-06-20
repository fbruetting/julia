# TerminalMenus

[![Build Status](https://travis-ci.org/nick-paul/TerminalMenus.jl.svg?branch=master)](https://travis-ci.org/nick-paul/TerminalMenus.jl)

[![Build status](https://ci.appveyor.com/api/projects/status/weaqa64co5boj87g?svg=true)](https://ci.appveyor.com/project/nick-paul/terminalmenus-jl)

![demo.gif](demo.gif)

TerminalMenus.jl is a small package that enables interactive menus in the terminal. This package is still in development. Multiple select, nested menus, and other menus will be added in the future.

## Example

```julia

using TerminalMenus

options = ["apple", "orange", "grape", "strawberry",
            "blueberry", "peach", "lemon", "lime"]

menu = RadioMenu(options, pagesize=4)

choice = request("Choose your favorite fruit:", menu)

if choice != -1
    println("Your favorite fruit is ", options[choice], "!")
else
    println("Menu canceled.")
end

```
