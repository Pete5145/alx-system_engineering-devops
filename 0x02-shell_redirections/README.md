**This script prints "Hello, World"** 0-hello_world

#!/bin/bash echo "Hello, World"

**This script displays a confused smiley to the output.** 2-confused_smiley

#!/bin/bash echo "(Ôo)' use ctrl, shift 6, capital O to get Ô

**This script displays the content of /etc/passwd** 2-hellofile

#!bin/bash cat /etc/passwd

**This script displays the contents of /etc/passwd and /etc/hosts** 3-twofiles

#!/bin/bash cat /etc/passwd /etc/hosts

**This script displays the last 10 lines of /etc/passwd** 4-lastlines

#!bin/bash tail /etc/passwd

**This script displays the first 10 lines of /etc/passwd** 5-firstlines

#!bin/bash head /etc/passwd

**This script displays the third line present in the iacta file** 6-third_line

#!/bin/bash cat iacta | head -n 3 | tail -n 1

**This script creates a file named \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing a text "Best School"** 7-file

#!/bin/bash echo "Best School" > \\\*\\\\"'\"Best School\"\\'"\\\\\*\$\\\?\\\*\\\*\\\*\\\*\\\*\:\)

**This script writes into the file ls_cwd_content the result of the command ls -la** 8-cwd_state

#!/bin/bash ls -la > ls_cwd_content

**This script duplicate the line line of the file iacta** 9-duplicate_last_line

#!/bin/bash tail -n 1 iacta >> iacta
     
**This script deletes all the regular files(not the directories) with a .js extension that are present in the current directory and sub folders** 10-no_more_js

#!/bin/bash
find . -type f -name '*.js' -delete

**This script counts the number of directories and sub-directories in the current directory** 11-directories

#!/bin/bash
find . -type d -not -name '.' | wc -l

**This script displays the 10 newest files in the current directory** 12-newest_files

#!/bin/bash
ls -t | head -n 10

**This script takes a list of words as input and prints only words that appear only once** 13-unique

#!/bin/bash
sort | uniq -u

**This script displays lines containing the pattern "root" from the file /etc/passwd** 14-findthatword

#!/bin/bash
grep "root" /etc/passwd

**This script displays the number of lines that contain the pattern "bin" in the file /etc/passwd** 15-countthatword

#!/bin/bash 
grep "bin" /etc/passwd | wc -l 

**This script displays lines containing the pattern "root" and 3 lines after them in the file /etc/passwd** 16-whatsnext

#!/bin/bash
grep -i "root" -A 3 /etc/passwd

**This script displays lines in file /etc/passwd that do not contain the pattern "bin"** 17-hidethisword

#!/bin/bash
grep -i -v "bin" /etc/passwd

**This script displays all lines of the file /etc/ssh/sshd_config starting with a letter** 18-letteronly

#!/bin/bash
grep -i "^[a-z]" /etc/ssh/sshd_config

**This script replace all characters A and c from input to Z and e respectively** 19-AZ

#!/bin/bash
tr "A" "Z" | tr "c" "e"

**This script removes all letters c and C from input** 20-hiago

#!/bin/bash
tr -d "cC"

**This script reverses its input** 21-reverse

#!/bin/bash
rev

**This script displays all users and their home directories, sorted by users.** 22-users_and_homes

#!/bin/bash
cut -d ":" -f 1,6 /etc/passwd | sort

**This script finds all empty files and directories in the current directory and all sub-directories** 100-empty_casks

#!/bin/bash
find . -empty | rev | cut -d '/' -f 1 | rev

**This script lists all the files with a .gif extension in the current directory and all its sub-directories.** 101-gifs

#!/bin/bash
find -type f -name '*.gif'|rev|cut -d '/' -f 1|cut -d '.' -f 2-|rev|LC_ALL=C sort -f  

**This script parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests.** 103-the_biggest_fan

#!/bin/bash                                                      
tail -n +2 | cut -f -1 | sort -k 1 | uniq -c | sort -rnk 1 | head -n 11 | rev | cut -d ' ' -f -1 | rev   







