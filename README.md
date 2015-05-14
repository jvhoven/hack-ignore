# Hack ignore

A simple module that reads out the .gitignore file.
This was mostly created for learning purposes.

## Usage

```
var gitignore = require("gitignore");

gitignore.read(function(err, data) {
	// where data is an array of all files and directories in your .gitignore
})

gitignore.sort(function(err, directories, files) {
	// directories are the directories inside your .gitignore
	// files are the files inside your .gitignore
})

## Known problem

The identification for a file or folder could be better, for example .git is a folder but will be treated as a file.
Still working on a way to fix this.