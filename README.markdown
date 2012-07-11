# diffnow-cli

**diffnow-cli** is a shell utility that enables you to compare files on [DiffNow](http://www.diffnow.com) from the command line.

Three output modes are supported:

- `diffnow file1 file2` outputs a short url to an online diff report hosted on diffnow.com for one week.
- `diffnow -o output file1 file2` downloads an HTML diff report to `output`.
- `diffnow -b browser file1 file2` downloads an HTML diff report to a temporary location and opens it with the specified browser.
