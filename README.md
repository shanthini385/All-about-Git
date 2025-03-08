# All-about-Git

## Installing Git

To install Git on Debian-based systems, use the following command:
```
sha@Shanthinid:~$ sudo apt-get install git
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Suggested packages:
  gettext-base git-daemon-run | git-daemon-sysvinit git-doc git-email git-gui gitk gitweb git-cvs git-mediawiki git-svn
The following NEW packages will be installed:
  git
0 upgraded, 1 newly installed, 0 to remove and 1 not upgraded.
Need to get 7,260 kB of archives.
After this operation, 46.0 MB of additional disk space will be used.
Get:1 http://security.debian.org/debian-security bookworm-security/main amd64 git amd64 1:2.39.5-0+deb12u2 [7,260 kB]
Fetched 7,260 kB in 1s (11.0 MB/s)
Selecting previously unselected package git.
(Reading database ... 173344 files and directories currently installed.)
Preparing to unpack .../git_1%3a2.39.5-0+deb12u2_amd64.deb ...
Unpacking git (1:2.39.5-0+deb12u2) ...
Setting up git (1:2.39.5-0+deb12u2) ...
sha@Shanthinid:~$
sha@Shanthinid:~$
```
After installing Git, set up your username and email (this will be linked to all commits).

```
sha@Shanthinid:~$ git --version
git version 2.39.5
sha@Shanthinid:~$ git config --global user.name "Shanthini"
sha@Shanthinid:~$ git config --global user.email "s10031996@gmail.com"
sha@Shanthinid:~$ git config --list
user.name=Shanthini
user.email=s10031996@gmail.com
sha@Shanthinid:~$
```
Aliases make Git commands shorter.

```
sha@Shanthinid:~$ git clone https://github.com/shanthini385/All-about-Git.git
Cloning into 'All-about-Git'...
remote: Enumerating objects: 18, done.
remote: Counting objects: 100% (18/18), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 18 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (18/18), 5.97 KiB | 679.00 KiB/s, done.
Resolving deltas: 100% (3/3), done.
sha@Shanthinid:~$ git config --global alias.s status
sha@Shanthinid:~$ git s
fatal: not a git repository (or any of the parent directories): .git
sha@Shanthinid:~$
sha@Shanthinid:~$ cd All-about-Git/
sha@Shanthinid:~/All-about-Git$
sha@Shanthinid:~/All-about-Git$ git s
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
sha@Shanthinid:~/All-about-Git$
```
Git hooks allow automation of tasks before or after commits, merges, or pushes.

```
sha@Shanthinid:~$ git clone https://github.com/shanthini385/All-about-Git.git
Cloning into 'All-about-Git'...
remote: Enumerating objects: 18, done.
remote: Counting objects: 100% (18/18), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 18 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (18/18), 5.97 KiB | 679.00 KiB/s, done.
Resolving deltas: 100% (3/3), done.
sha@Shanthinid:~$ git config --global alias.s status
sha@Shanthinid:~$ git s
fatal: not a git repository (or any of the parent directories): .git
sha@Shanthinid:~$
sha@Shanthinid:~$
sha@Shanthinid:~$
sha@Shanthinid:~$
sha@Shanthinid:~$
sha@Shanthinid:~$
sha@Shanthinid:~$ cd All-about-Git/
sha@Shanthinid:~/All-about-Git$
sha@Shanthinid:~/All-about-Git$
sha@Shanthinid:~/All-about-Git$
sha@Shanthinid:~/All-about-Git$ git s
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
sha@Shanthinid:~/All-about-Git$
sha@Shanthinid:~/All-about-Git$
sha@Shanthinid:~/All-about-Git$
sha@Shanthinid:~/All-about-Git$ ls -ltra
total 20
-rw-r--r--  1 sha sha   45 Mar  8 15:30 sample.txt
-rw-r--r--  1 sha sha 1471 Mar  8 15:30 README.md
drwxr-xr-x  3 sha sha 4096 Mar  8 15:30 .
drwx------ 11 sha sha 4096 Mar  8 15:30 ..
drwxr-xr-x  8 sha sha 4096 Mar  8 15:30 .git
sha@Shanthinid:~/All-about-Git$ cd .git
sha@Shanthinid:~/All-about-Git/.git$ ls -ltr
total 44
-rw-r--r-- 1 sha sha   73 Mar  8 15:30 description
drwxr-xr-x 2 sha sha 4096 Mar  8 15:30 info
drwxr-xr-x 2 sha sha 4096 Mar  8 15:30 hooks
drwxr-xr-x 2 sha sha 4096 Mar  8 15:30 branches
drwxr-xr-x 4 sha sha 4096 Mar  8 15:30 objects
drwxr-xr-x 5 sha sha 4096 Mar  8 15:30 refs
-rw-r--r-- 1 sha sha  112 Mar  8 15:30 packed-refs
-rw-r--r-- 1 sha sha   21 Mar  8 15:30 HEAD
drwxr-xr-x 3 sha sha 4096 Mar  8 15:30 logs
-rw-r--r-- 1 sha sha  270 Mar  8 15:30 config
-rw-r--r-- 1 sha sha  217 Mar  8 15:30 index
sha@Shanthinid:~/All-about-Git/.git$ cd hooks/
sha@Shanthinid:~/All-about-Git/.git/hooks$ ls -ltr
total 60
-rwxr-xr-x 1 sha sha 1374 Mar  8 15:30 pre-push.sample
-rwxr-xr-x 1 sha sha 1643 Mar  8 15:30 pre-commit.sample
-rwxr-xr-x 1 sha sha  189 Mar  8 15:30 post-update.sample
-rwxr-xr-x 1 sha sha  478 Mar  8 15:30 applypatch-msg.sample
-rwxr-xr-x 1 sha sha 3650 Mar  8 15:30 update.sample
-rwxr-xr-x 1 sha sha 2783 Mar  8 15:30 push-to-checkout.sample
-rwxr-xr-x 1 sha sha  544 Mar  8 15:30 pre-receive.sample
-rwxr-xr-x 1 sha sha 4898 Mar  8 15:30 pre-rebase.sample
-rwxr-xr-x 1 sha sha 1492 Mar  8 15:30 prepare-commit-msg.sample
-rwxr-xr-x 1 sha sha  416 Mar  8 15:30 pre-merge-commit.sample
-rwxr-xr-x 1 sha sha  424 Mar  8 15:30 pre-applypatch.sample
-rwxr-xr-x 1 sha sha 4726 Mar  8 15:30 fsmonitor-watchman.sample
-rwxr-xr-x 1 sha sha  896 Mar  8 15:30 commit-msg.sample
sha@Shanthinid:~/All-about-Git/.git/hooks$ vi pre-commit
sha@Shanthinid:~/All-about-Git/.git/hooks$ chmod +x pre-commit
sha@Shanthinid:~/All-about-Git/.git/hooks$ ls -lt
total 64
-rwxr-xr-x 1 sha sha   46 Mar  8 15:34 pre-commit
-rwxr-xr-x 1 sha sha  896 Mar  8 15:30 commit-msg.sample
-rwxr-xr-x 1 sha sha 4726 Mar  8 15:30 fsmonitor-watchman.sample
-rwxr-xr-x 1 sha sha  424 Mar  8 15:30 pre-applypatch.sample
-rwxr-xr-x 1 sha sha  416 Mar  8 15:30 pre-merge-commit.sample
-rwxr-xr-x 1 sha sha 1492 Mar  8 15:30 prepare-commit-msg.sample
-rwxr-xr-x 1 sha sha 4898 Mar  8 15:30 pre-rebase.sample
-rwxr-xr-x 1 sha sha  544 Mar  8 15:30 pre-receive.sample
-rwxr-xr-x 1 sha sha 2783 Mar  8 15:30 push-to-checkout.sample
-rwxr-xr-x 1 sha sha 3650 Mar  8 15:30 update.sample
-rwxr-xr-x 1 sha sha  478 Mar  8 15:30 applypatch-msg.sample
-rwxr-xr-x 1 sha sha  189 Mar  8 15:30 post-update.sample
-rwxr-xr-x 1 sha sha 1643 Mar  8 15:30 pre-commit.sample
-rwxr-xr-x 1 sha sha 1374 Mar  8 15:30 pre-push.sample
sha@Shanthinid:~/All-about-Git/.git/hooks$
sha@Shanthinid:~/All-about-Git/.git/hooks$ cd ..
sha@Shanthinid:~/All-about-Git/.git$ cd ..
sha@Shanthinid:~/All-about-Git$ ls -ltr
total 8
-rw-r--r-- 1 sha sha   45 Mar  8 15:30 sample.txt
-rw-r--r-- 1 sha sha 1471 Mar  8 15:30 README.md
sha@Shanthinid:~/All-about-Git$ vi sample.txt
sha@Shanthinid:~/All-about-Git$
sha@Shanthinid:~/All-about-Git$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   sample.txt

no changes added to commit (use "git add" and/or "git commit -a")
sha@Shanthinid:~/All-about-Git$ git add .
sha@Shanthinid:~/All-about-Git$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   sample.txt

sha@Shanthinid:~/All-about-Git$ git commit -m "Initial commit"
Running pre-commit hook...
[main 4980fdf] Initial commit
 1 file changed, 1 insertion(+), 1 deletion(-)
sha@Shanthinid:~/All-about-Git$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
sha@Shanthinid:~/All-about-Git$ git log --oneline
4980fdf (HEAD -> main) Initial commit
0195d7c (origin/main, origin/HEAD) Create sample.txt
bc5969f Update README.md
3b2ffdd Update README.md
bdbea8c Update README.md
95e24db Update README.md
5eb4770 Initial commit
sha@Shanthinid:~/All-about-Git$ git log
commit 4980fdfdaf13debe073aa567be468cbcaf69d095 (HEAD -> main)
Author: Shanthini <s10031996@gmail.com>
Date:   Sat Mar 8 15:37:41 2025 -0600

    Initial commit

commit 0195d7c660dd0a24f4d72f72ff3a1b091a537fdf (origin/main, origin/HEAD)
Author: Shanthini <s10031996@gmail.com>
Date:   Sat Mar 8 15:29:24 2025 -0600

    Create sample.txt

commit bc5969f60d49ad953edeb6a4b078b1faa918d1aa
Author: Shanthini <s10031996@gmail.com>
Date:   Sat Mar 8 15:03:24 2025 -0600

    Update README.md

commit 3b2ffddcfe9f87edbf45174bf802d098ea19ce0d
Author: Shanthini <s10031996@gmail.com>
Date:   Sat Mar 8 15:01:14 2025 -0600

    Update README.md

commit bdbea8c24b1e864a820493bbf16aac11553a1e73
Author: Shanthini <s10031996@gmail.com>
Date:   Sat Mar 8 15:01:02 2025 -0600

    Update README.md

commit 95e24db5bb652def638c6a46be5500c8fa5e71de
Author: Shanthini <s10031996@gmail.com>
Date:   Sat Mar 8 15:00:46 2025 -0600

    Update README.md

commit 5eb47704a27b2962ba921fa10dd3004f939bdeaa
Author: Shanthini <s10031996@gmail.com>
Date:   Sat Mar 8 14:52:58 2025 -0600

    Initial commit
sha@Shanthinid:~/All-about-Git$ git log --oneline
4980fdf (HEAD -> main) Initial commit
0195d7c (origin/main, origin/HEAD) Create sample.txt
bc5969f Update README.md
3b2ffdd Update README.md
bdbea8c Update README.md
95e24db Update README.md
5eb4770 Initial commit
sha@Shanthinid:~/All-about-Git$
```
