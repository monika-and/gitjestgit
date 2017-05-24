# gitjestgit
Windows PowerShell
Copyright (C) 2014 Microsoft Corporation. All rights reserved.

~\Documents\GitHub> cd 'C:\Users\anra6003\Desktop\repo-git'
~\Desktop\repo-git> git clone https://github.com/monika-and/gitjestgit
Cloning into 'gitjestgit'...
warning: You appear to have cloned an empty repository.
~\Desktop\repo-git> cd 'gitjestgit'
~\Desktop\repo-git\gitjestgit [master]> mkdir 'pliki'


    Directory: C:\Users\anra6003\Desktop\repo-git\gitjestgit


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        2017-05-24     22:12            pliki


~\Desktop\repo-git\gitjestgit [master]> cd 'pliki'
~\Desktop\repo-git\gitjestgit\pliki [master]> touch 'plik1.html'
~\Desktop\repo-git\gitjestgit\pliki [master +1 ~0 -0 !]> touch 'plik2.html'
~\Desktop\repo-git\gitjestgit\pliki [master +1 ~0 -0 !]> ls


    Directory: C:\Users\anra6003\Desktop\repo-git\gitjestgit\pliki


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
-a---        2017-05-24     22:15          0 plik1.html
-a---        2017-05-24     22:15          0 plik2.html


~\Desktop\repo-git\gitjestgit\pliki [master +1 ~0 -0 !]> cd ..
~\Desktop\repo-git\gitjestgit [master +1 ~0 -0 !]> touch 'indwx.html'
~\Desktop\repo-git\gitjestgit [master +2 ~0 -0 !]> rm 'indwx.html'
~\Desktop\repo-git\gitjestgit [master +1 ~0 -0 !]> touch 'index.html'
~\Desktop\repo-git\gitjestgit [master +2 ~0 -0 !]> ls


    Directory: C:\Users\anra6003\Desktop\repo-git\gitjestgit


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        2017-05-24     22:15            pliki
-a---        2017-05-24     22:20          0 index.html


~\Desktop\repo-git\gitjestgit [master +2 ~0 -0 !]> git add*
git: 'add*' is not a git command. See 'git --help'.

Did you mean this?
        add
~\Desktop\repo-git\gitjestgit [master +2 ~0 -0 !]> git add *
~\Desktop\repo-git\gitjestgit [master +3 ~0 -0 ~]> git commit -m'init'
[master (root-commit) 4ad7dbd] init
 3 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 index.html
 create mode 100644 pliki/plik1.html
 create mode 100644 pliki/plik2.html
~\Desktop\repo-git\gitjestgit [master ×]> git push
Counting objects: 4, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 307 bytes | 0 bytes/s, done.
Total 4 (delta 0), reused 0 (delta 0)
To https://github.com/monika-and/gitjestgit
 * [new branch]      master -> master
~\Desktop\repo-git\gitjestgit [master ?]> git checkout -b 'version2'
Switched to a new branch 'version2'
~\Desktop\repo-git\gitjestgit [version2]> git add *
~\Desktop\repo-git\gitjestgit [version2 +0 ~1 -0 ~]> git commit -m'drugi paragraf'
[version2 4721449] drugi paragraf
 1 file changed, 11 insertions(+)
~\Desktop\repo-git\gitjestgit [version2]> git checkout master
Your branch is up-to-date with 'origin/master'.
Switched to branch 'master'
~\Desktop\repo-git\gitjestgit [master ?]> git add *
~\Desktop\repo-git\gitjestgit [master ? +0 ~1 -0 ~]> git commit -m'trzeci paragraf'
[master 9970221] trzeci paragraf
 1 file changed, 11 insertions(+)
~\Desktop\repo-git\gitjestgit [master ↑1]> git merge master version2
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
~\Desktop\repo-git\gitjestgit [master ↑1 +0 ~0 -0 !1 | +0 ~0 -0 !1 !]> git add *
~\Desktop\repo-git\gitjestgit [master ↑1 +0 ~1 -0 ~]> git commit -m'Merged master with version2'
[master 57f2599] Merged master with version2
~\Desktop\repo-git\gitjestgit [master ↑3]> git push
Counting objects: 9, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 952 bytes | 0 bytes/s, done.
Total 9 (delta 3), reused 0 (delta 0)
remote: Resolving deltas: 100% (3/3), done.
To https://github.com/monika-and/gitjestgit
   4ad7dbd..57f2599  master -> master
~\Desktop\repo-git\gitjestgit [master ?]> git checkout version2
Switched to branch 'version2'
~\Desktop\repo-git\gitjestgit [version2]> git push
fatal: The current branch version2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin version2

~\Desktop\repo-git\gitjestgit [version2]> git checkout master
Your branch is up-to-date with 'origin/master'.
Switched to branch 'master'
~\Desktop\repo-git\gitjestgit [master ?]> git checkout version2
Switched to branch 'version2'
~\Desktop\repo-git\gitjestgit [version2]> git push --set-upstream origin version2
Total 0 (delta 0), reused 0 (delta 0)
Branch version2 set up to track remote branch version2 from origin.
To https://github.com/monika-and/gitjestgit
 * [new branch]      version2 -> version2
~\Desktop\repo-git\gitjestgit [version2 ?]>

