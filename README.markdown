# diffnow-cli

**diffnow-cli** is a shell utility that enables you to compare files on [DiffNow](http://www.diffnow.com) from the command line.

Three output modes are supported:

- `diffnow file1 file2` outputs a short url to an online diff report hosted on diffnow.com for one week.
- `diffnow -o output file1 file2` downloads an HTML diff report to `output`.
- `diffnow -b browser file1 file2` downloads an HTML diff report to a temporary location and opens it with the specified browser.

## Using diffnow-cli with git

I've added the following lines to my global `.gitconfig` file:

```
[diff]
	tool = diffnow
[difftool "diffnow"]
	cmd = diffnow -b chromium $LOCAL $REMOTE
[difftool]
	prompt = false
```

Now I can compare a file to its previous version by running:

```
git difftool --gui <file>
```
