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
