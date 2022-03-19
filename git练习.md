zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode
$ git init
Initialized empty Git repository in C:/gitcode/.git/

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ touch readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git add readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   readme.txt


zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git commit -m 'readme.txt'
[master (root-commit) 50d337c] readme.txt
 1 file changed, 1 insertion(+)
 create mode 100644 readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git status
On branch master
nothing to commit, working tree clean

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git diff readme.txt
diff --git a/readme.txt b/readme.txt
index b23c1c5..b72ce18 100644
--- a/readme.txt
+++ b/readme.txt
@@ -1 +1,2 @@
-111111
\ No newline at end of file
+111111
+222222
\ No newline at end of file

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git add readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git commit -m 'readme.txt'
[master 925e88e] readme.txt
 1 file changed, 2 insertions(+), 1 deletion(-)

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git add readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git commit -m 'readme.txt'
[master 3bd3526] readme.txt
 1 file changed, 2 insertions(+), 1 deletion(-)

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git log
commit 3bd352680ef1596699637575c4efc40b8e89f632 (HEAD -> master)
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:21:23 2022 +0800

    readme.txt

commit 925e88e47f37a1121f3a050ca1b3bc343e71cc1c
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:19:47 2022 +0800

    readme.txt

commit 50d337cbdb21472bac287333c2e429c478fd2264
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:18:00 2022 +0800

    readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git log --pretty=online
fatal: invalid --pretty format: online

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git log --pretty=oneline
3bd352680ef1596699637575c4efc40b8e89f632 (HEAD -> master) readme.txt
925e88e47f37a1121f3a050ca1b3bc343e71cc1c readme.txt
50d337cbdb21472bac287333c2e429c478fd2264 readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git reset --hard HEAD^
HEAD is now at 925e88e readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ cat readme.txt
111111
222222
zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git log
commit 925e88e47f37a1121f3a050ca1b3bc343e71cc1c (HEAD -> master)
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:19:47 2022 +0800

    readme.txt

commit 50d337cbdb21472bac287333c2e429c478fd2264
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:18:00 2022 +0800

    readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git reflog
925e88e (HEAD -> master) HEAD@{0}: reset: moving to HEAD^
3bd3526 HEAD@{1}: commit: readme.txt
925e88e (HEAD -> master) HEAD@{2}: commit: readme.txt
50d337c HEAD@{3}: commit (initial): readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git reset --hard 3bd3526
HEAD is now at 3bd3526 readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ cat readme.txt
111111
222222
333333
zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ touch test.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   readme.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test.txt

no changes added to commit (use "git add" and/or "git commit -a")

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git add readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git add test.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   readme.txt
        new file:   test.txt


zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git commit -m "一次性提交所有文件，包括新建文件test.txt"
[master 15c5b00] 一次性提交所有文件，包括新建文件test.txt
 2 files changed, 3 insertions(+), 1 deletion(-)
 create mode 100644 test.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ cat readme.txt
111111
222222
333333
444444
555555
zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git checkout -- readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ cat readme.txt
111111
222222
333333
444444
zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git add readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ cat readme.txt
111111
222222
333333
444444
666666
777777
zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git checkout -- readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ cat readme.txt
111111
222222
333333
444444
666666
zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ touch b.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git add b.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git commit -m "添加b.txt文件"
[master 11c064e] 添加b.txt文件
 2 files changed, 2 insertions(+), 1 deletion(-)
 create mode 100644 b.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ rm b.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    b.txt

no changes added to commit (use "git add" and/or "git commit -a")

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git checkout -- b.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ ssh-keygen -t rsa -C"ad19836229566@qq.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/zhu_j/.ssh/id_rsa):
/c/Users/zhu_j/.ssh/id_rsa already exists.
Overwrite (y/n)?


zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git config --global user.name "zj1982"

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git config --global user,email "ad19836229566@qq.com"
error: key does not contain a section: user,email

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git config --global user.email "ad19836229566@qq.com"

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git config --global user.email "ad19836229566@qq.com"

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git remote add origin https://github.com/zj1982/gitcode.git

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git push -u origin master
fatal: unable to access 'https://github.com/zj1982/gitcode.git/': OpenSSL SSL_read: Connection was reset, errno 10054

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git config --global user.name "zj1982"

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git config --global user.email "ad19836229566@qq.com"

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ ssh-keygen -t rsa -C"ad19836229566@qq.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/zhu_j/.ssh/id_rsa):
Created directory '/c/Users/zhu_j/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/zhu_j/.ssh/id_rsa
Your public key has been saved in /c/Users/zhu_j/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:MsV7QXv9/LZ6WIIwrVlOlUPYGVHM5vkzxh3QtjX0JxY ad19836229566@qq.com
The key's randomart image is:
+---[RSA 3072]----+
|          . ++Eo |
|       . . o O Oo|
|        o + o X B|
|       . + * . O.|
|      o S X . . *|
|       o + o . *+|
|              = =|
|             . o.|
|             .o. |
+----[SHA256]-----+

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git remote add origin https://github.com/zj1982/gitcode1.git
error: remote origin already exists.

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git push -u origin master
info: please complete authentication in your browser...
Enumerating objects: 17, done.
Counting objects: 100% (17/17), done.
Delta compression using up to 12 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (17/17), 1.25 KiB | 425.00 KiB/s, done.
Total 17 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/zj1982/gitcode.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git clone https://github.com/zj1982/gitcode2.git
Cloning into 'gitcode2'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git checkout -b dev
Switched to a new branch 'dev'

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (dev)
$ git branch
* dev
  master

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (dev)
$ cat readme.txt
111111
222222
333333
444444
666666
777777
zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (dev)
$ git add readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (dev)
$ git commit -m "dev分支上增加内容777777"
[dev 0148763] dev分支上增加内容777777
 1 file changed, 2 insertions(+), 1 deletion(-)

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (dev)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ cat readme.txt
111111
222222
333333
444444
666666
zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git merge dev
Updating 11c064e..0148763
Fast-forward
 readme.txt | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ cat readme.txt
111111
222222
333333
444444
666666
777777
zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git branch -d dev
Deleted branch dev (was 0148763).

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git branch
* master

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git branch -b fenzhi1
error: unknown switch `b'
usage: git branch [<options>] [-r | -a] [--merged] [--no-merged]
   or: git branch [<options>] [-l] [-f] <branch-name> [<start-point>]
   or: git branch [<options>] [-r] (-d | -D) <branch-name>...
   or: git branch [<options>] (-m | -M) [<old-branch>] <new-branch>
   or: git branch [<options>] (-c | -C) [<old-branch>] <new-branch>
   or: git branch [<options>] [-r | -a] [--points-at]
   or: git branch [<options>] [-r | -a] [--format]

Generic options
    -v, --verbose         show hash and subject, give twice for upstream branch
    -q, --quiet           suppress informational messages
    -t, --track[=(direct|inherit)]
                          set branch tracking configuration
    -u, --set-upstream-to <upstream>
                          change the upstream info
    --unset-upstream      unset the upstream info
    --color[=<when>]      use colored output
    -r, --remotes         act on remote-tracking branches
    --contains <commit>   print only branches that contain the commit
    --no-contains <commit>
                          print only branches that don't contain the commit
    --abbrev[=<n>]        use <n> digits to display object names

Specific git-branch actions:
    -a, --all             list both remote-tracking and local branches
    -d, --delete          delete fully merged branch
    -D                    delete branch (even if not merged)
    -m, --move            move/rename a branch and its reflog
    -M                    move/rename a branch, even if target exists
    -c, --copy            copy a branch and its reflog
    -C                    copy a branch, even if target exists
    -l, --list            list branch names
    --show-current        show current branch name
    --create-reflog       create the branch's reflog
    --edit-description    edit the description for the branch
    -f, --force           force creation, move/rename, deletion
    --merged <commit>     print only branches that are merged
    --no-merged <commit>  print only branches that are not merged
    --column[=<style>]    list branches in columns
    --sort <key>          field name to sort on
    --points-at <object>  print only branches of the object
    -i, --ignore-case     sorting and filtering are case insensitive
    --format <format>     format to use for the output


zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git checkout -b fenzhi1
Switched to a new branch 'fenzhi1'

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (fenzhi1)
$ cat readme.txt
111111
222222
333333
444444
666666
777777
zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (fenzhi1)
$ cat readme.txt
111111
222222
333333
444444
666666
777777
888888
zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (fenzhi1)
$ git add readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (fenzhi1)
$ git commit -m "添加内容888888"
[fenzhi1 6eac532] 添加内容888888
 1 file changed, 2 insertions(+), 1 deletion(-)

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (fenzhi1)
$ git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ cat readme.txt
111111
222222
333333
444444
666666
777777
999999
zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git add readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git commit -m "master加999999"
[master 2aecb64] master加999999
 1 file changed, 2 insertions(+), 1 deletion(-)

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git merge fenzhi1
Auto-merging readme.txt
CONFLICT (content): Merge conflict in readme.txt
Automatic merge failed; fix conflicts and then commit the result.

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master|MERGING)
$ git ststus
git: 'ststus' is not a git command. See 'git --help'.

The most similar command is
        status

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master|MERGING)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   readme.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        gitcode2/

no changes added to commit (use "git add" and/or "git commit -a")

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master|MERGING)
$ cat readme.txt
111111
222222
333333
444444
666666
777777
<<<<<<< HEAD
999999
=======
888888
>>>>>>> fenzhi1

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master|MERGING)
$ cat readme.txt
111111
222222
333333
444444
666666
777777
<<<<<<< HEAD
999999
=======
888888
>>>>>>> fenzhi1

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master|MERGING)
$ cat readme.txt
111111
222222
333333
444444
666666
777777
999999

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master|MERGING)
$ git add readme.txt

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master|MERGING)
$ git commit -m "conflit fixed"
[master 2d0b693] conflit fixed

zhu_j@LAPTOP-N2QFRI4P MINGW64 /c/gitcode (master)
$ git log
commit 2d0b6930eb75036f47a605987bc6b1305e66d976 (HEAD -> master)
Merge: 2aecb64 6eac532
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:43:51 2022 +0800

    conflit fixed

commit 2aecb646509c45d2c0af07dfd7ddeb3647c2d30c
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:37:45 2022 +0800

    master加999999

commit 6eac5320fe4fdd3aba022f50d56ec56422ace64f (fenzhi1)
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:35:49 2022 +0800

    添加内容888888

commit 0148763c5507267e8ff80aa763a92441fefb8836
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:29:25 2022 +0800

    dev分支上增加内容777777

commit 11c064e6536701350366c11ebea9038469e4db38 (origin/master)
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:43:18 2022 +0800

    添加b.txt文件


commit 2d0b6930eb75036f47a605987bc6b1305e66d976 (HEAD -> master)
Merge: 2aecb64 6eac532
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:43:51 2022 +0800

    conflit fixed

commit 2aecb646509c45d2c0af07dfd7ddeb3647c2d30c
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:37:45 2022 +0800

    master加999999

commit 6eac5320fe4fdd3aba022f50d56ec56422ace64f (fenzhi1)
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:35:49 2022 +0800

    添加内容888888

commit 0148763c5507267e8ff80aa763a92441fefb8836
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:29:25 2022 +0800

    dev分支上增加内容777777

commit 11c064e6536701350366c11ebea9038469e4db38 (origin/master)
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:43:18 2022 +0800

    添加b.txt文件

commit 15c5b004fd82e93f683f6b83189a0f1211cf8d7a
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:35:05 2022 +0800

    一次性提交所有文件，包括新建文件test.txt

commit 3bd352680ef1596699637575c4efc40b8e89f632
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:21:23 2022 +0800

    readme.txt

commit 925e88e47f37a1121f3a050ca1b3bc343e71cc1c
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:19:47 2022 +0800

...skipping...

commit 11c064e6536701350366c11ebea9038469e4db38 (origin/master)
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:43:18 2022 +0800

    添加b.txt文件

commit 15c5b004fd82e93f683f6b83189a0f1211cf8d7a
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:35:05 2022 +0800

    一次性提交所有文件，包括新建文件test.txt

commit 3bd352680ef1596699637575c4efc40b8e89f632
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:21:23 2022 +0800

    readme.txt

commit 925e88e47f37a1121f3a050ca1b3bc343e71cc1c
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:19:47 2022 +0800
commit 2d0b6930eb75036f47a605987bc6b1305e66d976 (HEAD -> master)
Merge: 2aecb64 6eac532
commit 2d0b6930eb75036f47a605987bc6b1305e66d976 (HEAD -> master)
Merge: 2aecb64 6eac532
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:43:51 2022 +0800

    conflit fixed

commit 2aecb646509c45d2c0af07dfd7ddeb3647c2d30c
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:37:45 2022 +0800

    master加999999

commit 6eac5320fe4fdd3aba022f50d56ec56422ace64f (fenzhi1)
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:35:49 2022 +0800

    添加内容888888

commit 0148763c5507267e8ff80aa763a92441fefb8836
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:29:25 2022 +0800

    dev分支上增加内容777777

commit 11c064e6536701350366c11ebea9038469e4db38 (origin/master)
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 16:43:18 2022 +0800

    添加b.txt文件

commit 2d0b6930eb75036f47a605987bc6b1305e66d976 (HEAD -> master)
Merge: 2aecb64 6eac532
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:43:51 2022 +0800

    conflit fixed

commit 2aecb646509c45d2c0af07dfd7ddeb3647c2d30c
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:37:45 2022 +0800

    master加999999

commit 6eac5320fe4fdd3aba022f50d56ec56422ace64f (fenzhi1)
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:35:49 2022 +0800

    添加内容888888

commit 0148763c5507267e8ff80aa763a92441fefb8836
Author: zj1982 <ad19836229566@qq.com>
Date:   Sat Mar 19 17:29:25 2022 +0800

: