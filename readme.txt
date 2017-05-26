Git is a distributed version control system
Git is free software


hoto@boc MINGW64 ~
$ git config --global user.name "vsion"

hoto@boc MINGW64 ~
$ git config --global user.email "vsion@qq.com"

hoto@boc MINGW64 ~
$ mkdir learngit

hoto@boc MINGW64 ~
$ dir
;
_viminfo
¡¸¿ªÊ¼¡¹²Ëµ¥
3D\ Objects
AppData
Application\ Data
AwesomeProject
Contacts
Cookies
Desktop
Documents
Downloads
Favorites
IntelGraphicsProfiles
learngit
Links
Local\ Settings
LocalStorage
mercurial.ini
Music
My\ Documents
NetHood
NTUSER.DAT
ntuser.dat.LOG1
ntuser.dat.LOG2
NTUSER.DAT{3c0b22bf-bb61-11e6-b20b-dab0704102a2}.TM.blf
NTUSER.DAT{3c0b22bf-bb61-11e6-b20b-dab0704102a2}.TMContainer0000000000.regtrans-ms
NTUSER.DAT{3c0b22bf-bb61-11e6-b20b-dab0704102a2}.TMContainer0000000000.regtrans-ms
ntuser.ini
OneDrive
Pictures
PrintHood
Program\ Files
Recent
Roaming
Saved\ Games
Searches
SendTo
Templates
test
Videos
wc
WebpageIcons.db
workspace
yqProject

hoto@boc MINGW64 ~
$ cd learngit/

hoto@boc MINGW64 ~/learngit
$ pwd
/c/Users/hoto/learngit

hoto@boc MINGW64 ~/learngit
$ cd e
bash: cd: e: No such file or directory

hoto@boc MINGW64 ~/learngit
$ cd e:

hoto@boc MINGW64 /e
$ pwd
/e

hoto@boc MINGW64 /e
$ mkdir learngit

hoto@boc MINGW64 /e
$ cd learngit/

hoto@boc MINGW64 /e/learngit
$ pwd
/e/learngit

hoto@boc MINGW64 /e/learngit
$ git init
Initialized empty Git repository in E:/learngit/.git/

hoto@boc MINGW64 /e/learngit (master)
$ ^C

hoto@boc MINGW64 /e/learngit (master)
$ ls -ah
./  ../  .git/

hoto@boc MINGW64 /e/learngit (master)
$ git add readme.txt

hoto@boc MINGW64 /e/learngit (master)
$ git commit -m "write a readme file"
[master (root-commit) 91769f0] write a readme file
 1 file changed, 2 insertions(+)
 create mode 100644 readme.txt

hoto@boc MINGW64 /e/learngit (master)
$ git add hello.txt -m "add hello"
error: unknown switch `m'
usage: git add [<options>] [--] <pathspec>...

    -n, --dry-run         dry run
    -v, --verbose         be verbose

    -i, --interactive     interactive picking
    -p, --patch           select hunks interactively
    -e, --edit            edit current diff and apply
    -f, --force           allow adding otherwise ignored files
    -u, --update          update tracked files
    -N, --intent-to-add   record only the fact that the path will be a
    -A, --all             add changes from all tracked and untracked f
    --ignore-removal      ignore paths removed in the working tree (sa-all)
    --refresh             don't add, only refresh the index
    --ignore-errors       just skip files which cannot be added becauss
    --ignore-missing      check if - even missing - files are ignored


hoto@boc MINGW64 /e/learngit (master)
$ git add hello.txt

hoto@boc MINGW64 /e/learngit (master)
$ git add readme.txt

hoto@boc MINGW64 /e/learngit (master)
$ git commit -m "add 2 file"
[master 08e0f4e] add 2 file
 1 file changed, 1 insertion(+)
 create mode 100644 hello.txt

hoto@boc MINGW64 /e/learngit (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")

hoto@boc MINGW64 /e/learngit (master)
$ git diff readme.txt
diff --git a/readme.txt b/readme.txt
index fe0ef79..be836b4 100644
--- a/readme.txt
+++ b/readme.txt
@@ -1,2 +1,2 @@
-Git is version control system
+Git is a distributed version control system
 Git is free software
\ No newline at end of file

hoto@boc MINGW64 /e/learngit (master)
$ git add readme.txt

hoto@boc MINGW64 /e/learngit (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   readme.txt


hoto@boc MINGW64 /e/learngit (master)
$ gti commit -m "add distributed"
bash: gti: command not found

hoto@boc MINGW64 /e/learngit (master)
$ git commit -m "add distributed"
[master eea5411] add distributed
 1 file changed, 1 insertion(+), 1 deletion(-)

hoto@boc MINGW64 /e/learngit (master)
$ git status
On branch master
nothing to commit, working directory clean

hoto@boc MINGW64 /e/learngit (master)
$ git status
On branch master
nothing to commit, working directory clean

hoto@boc MINGW64 /e/learngit (master)
$ git log
commit eea54115904927945159f6b9500a49022c9ced10
Author: vsion <vsion@qq.com>
Date:   Thu May 25 18:34:57 2017 +0800

    add distributed

commit 08e0f4e10be5650b10fd631096a8e98c0ddff537
Author: vsion <vsion@qq.com>
Date:   Thu May 25 18:26:45 2017 +0800

    add 2 file

commit 91769f0fbe5f55f3ea3c978988846dcb1e2a0fe9
Author: vsion <vsion@qq.com>
Date:   Thu May 25 18:23:22 2017 +0800

    write a readme file

hoto@boc MINGW64 /e/learngit (master)
$ git log --pretty=oneline
eea54115904927945159f6b9500a49022c9ced10 add distributed
08e0f4e10be5650b10fd631096a8e98c0ddff537 add 2 file
91769f0fbe5f55f3ea3c978988846dcb1e2a0fe9 write a readme file

hoto@boc MINGW64 /e/learngit (master)
$ git reset --hard HEAD
HEAD is now at eea5411 add distributed

hoto@boc MINGW64 /e/learngit (master)
$ cat readme.txt
Git is a distributed version control system
Git is free software
hoto@boc MINGW64 /e/learngit (master)
$ git log
commit eea54115904927945159f6b9500a49022c9ced10
Author: vsion <vsion@qq.com>
Date:   Thu May 25 18:34:57 2017 +0800

    add distributed

commit 08e0f4e10be5650b10fd631096a8e98c0ddff537
Author: vsion <vsion@qq.com>
Date:   Thu May 25 18:26:45 2017 +0800

    add 2 file

commit 91769f0fbe5f55f3ea3c978988846dcb1e2a0fe9
Author: vsion <vsion@qq.com>
Date:   Thu May 25 18:23:22 2017 +0800

    write a readme file

hoto@boc MINGW64 /e/learngit (master)
$ git reset --hard eea
fatal: ambiguous argument 'eea': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

hoto@boc MINGW64 /e/learngit (master)
$ git reset --hard 'eea'
fatal: ambiguous argument 'eea': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

hoto@boc MINGW64 /e/learngit (master)
$ git reset --hard eea5411
HEAD is now at eea5411 add distributed

hoto@boc MINGW64 /e/learngit (master)
$ cat readme.txt
Git is a distributed version control system
Git is free software
hoto@boc MINGW64 /e/learngit (master)
$ git
usage: git [--version] [--help] [-C <path>] [-c name=value]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone      Clone a repository into a new directory
   init       Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add        Add file contents to the index
   mv         Move or rename a file, a directory, or a symlink
   reset      Reset current HEAD to the specified state
   rm         Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect     Use binary search to find the commit that introduced a bug
   grep       Print lines matching a pattern
   log        Show commit logs
   show       Show various types of objects
   status     Show the working tree status

grow, mark and tweak your common history
   branch     List, create, or delete branches
   checkout   Switch branches or restore working tree files
   commit     Record changes to the repository
   diff       Show changes between commits, commit and working tree, etc
   merge      Join two or more development histories together
   rebase     Forward-port local commits to the updated upstream head
   tag        Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch      Download objects and refs from another repository
   pull       Fetch from and integrate with another repository or a local branch
   push       Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.

hoto@boc MINGW64 /e/learngit (master)
$ git reset --hard head^
HEAD is now at 08e0f4e add 2 file

hoto@boc MINGW64 /e/learngit (master)
$ cat readme.txt
Git is version control system
Git is free software
hoto@boc MINGW64 /e/learngit (master)
$ git reset --hard 917
fatal: ambiguous argument '917': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

hoto@boc MINGW64 /e/learngit (master)
$ git reset --hard 91769
HEAD is now at 91769f0 write a readme file

hoto@boc MINGW64 /e/learngit (master)
$ git reflog
91769f0 HEAD@{0}: reset: moving to 91769
08e0f4e HEAD@{1}: reset: moving to head^
eea5411 HEAD@{2}: commit: add distributed
08e0f4e HEAD@{3}: commit: add 2 file
91769f0 HEAD@{4}: commit (initial): write a readme file

hoto@boc MINGW64 /e/learngit (master)
$ git reset --hard eea5411
HEAD is now at eea5411 add distributed