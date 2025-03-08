# All-about-Git
=========================

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
