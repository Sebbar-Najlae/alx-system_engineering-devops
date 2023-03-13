# 0x02-shell_redirections

Explanation of the command file gif:

* find . -type f -name "*.gif": This finds all the regular files with .gif extension in the current directory and its subdirectories.
* sed 's/\.[^.]*$//': This removes the file extension from each file name.
* sort -f: This sorts the file names in case-insensitive order.
* sort -n: This sorts the file names by byte values.
* tr '\n' '\0': This replaces newlines with null characters, allowing for handling of filenames with spaces.
* xargs -0 -I {} echo {}: This prints each file name on a separate line.
Note: This command assumes that there are no newlines in the file names.
