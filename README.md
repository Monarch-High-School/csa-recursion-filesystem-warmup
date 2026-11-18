# Recursion in a file system

Complete `printTextFiles(String folder)` in `PrintTextFiles.java`.
Print the path of each text file in the supplied toy filesystem, including files in nested folders.
Print each path once, on its own line. Use recursion. Loops may visit the items in one folder.
Keep the five supplied API methods unchanged. No arrays are needed in your method.

## Open and run

Use a private copy of this starter in `Monarch-High-School`.
Name it `recursion-warmup-YOUR-GITHUB-USERNAME`.
Keep an existing copy and its commits if you already have one.
Open that copy in Codespaces or clone it into VS Code.

Open a terminal in the repository's top folder.

```sh
javac FileSystem.java PrintTextFiles.java
java PrintTextFiles
```

The starter compiles. It prints immediate items, including folders and non-text files.
It does not yet meet the task.

## Folder API

An API is the set of supplied methods your code can call.
Paths are Strings. Each `item` call returns one String.

| Call | Result |
|---|---|
| `FileSystem.root()` | The top folder's path |
| `FileSystem.count(folder)` | Number of immediate items, including files and folders |
| `FileSystem.item(folder, i)` | Path of immediate item number `i` |
| `FileSystem.isFolder(path)` | Whether this path is a folder |
| `FileSystem.isTextFile(path)` | Whether this path is a file ending with lowercase `.txt` |

Item numbers start at 0 and stop at `count(folder) - 1`.
For an empty folder, `count` returns 0. There is no valid item number.
Each folder lists items in alphabetical name order.
The supplied API ignores `.gitkeep`, which preserves an empty folder in Git.
Use the toy folders as supplied. Keep the tree unchanged during a run.

## Check the result

The completed method prints exactly these five paths in this order:

```text
toy-filesystem/home/music/old/lyrics.txt
toy-filesystem/home/music/playlist.txt
toy-filesystem/home/readme.txt
toy-filesystem/home/school/csa/notes.txt
toy-filesystem/home/school/schedule.txt
```

It prints no folder paths and no non-text files. The empty folder produces no output.
It prints file names with their paths, rather than file contents.
Compare the result with your partner pseudocode.

## Explain and save

Identify the Big 4 in your method:

1. The method calls itself.
2. Each subsequent call works on a smaller version of the same task.
3. A base case stops the calls.
4. Each call waits for the next call, then finishes its own work.

Explain where the current call continues after a subfolder call returns.
Save, test, commit, and push your change to your own repository.
Open the pushed commit on GitHub and show Archer its link.
