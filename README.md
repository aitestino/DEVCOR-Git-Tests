# DEVCOR-Git-Tests
DEVCOR Blueprint 1.10 "Advanced VC operations with Git"

#### Create a branch called feature and merge said 'feature' to 'master' branch ####

```
ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ ls
README.md		this-is-a-test.txt
ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ git checkout -b feature master
M	this-is-a-test.txt
Switched to a new branch 'feature'


ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ vi this-is-a-test.txt 
# Added a line here (file was empty prior to this)
ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ git add this-is-a-test.txt 
ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ git commit 
[feature 1b5886c] Added a line to the file this-is-a-test.txt
 1 file changed, 1 insertion(+)


ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ git status
On branch feature
nothing to commit, working tree clean

ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ git log
commit 1b5886cb7cc25db5c400dc0ebcd07d1486a3cca4 (HEAD -> feature)
Author: Andrea Testino <atestini@cisco.com>
Date:   Mon Feb 28 20:58:39 2022 -0500

    Added a line to the file this-is-a-test.txt

commit 72094085090e797d0148b5105b581e934779329f (origin/master, origin/HEAD, master)
Author: Andrea Testino <atestini@cisco.com>
Date:   Mon Feb 28 20:55:51 2022 -0500

    Adding empty file for later test

commit f82f85402b3606855e0d6669bc86cf922a6bd934
Author: aitestino <59578890+aitestino@users.noreply.github.com>
Date:   Mon Feb 28 20:48:41 2022 -0500

    Initial commit


ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.


ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ git merge --no-ff feature
Merge made by the 'recursive' strategy.
 this-is-a-test.txt | 1 +
 1 file changed, 1 insertion(+)


ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ git log
commit 8d11c18b33c2cc8bd1a484a148a718683cdc891c (HEAD -> master)
Merge: 7209408 1b5886c
Author: Andrea Testino <atestini@cisco.com>
Date:   Mon Feb 28 20:59:26 2022 -0500

    Testing --no-ff kw
    
    Merge branch 'feature'

commit 1b5886cb7cc25db5c400dc0ebcd07d1486a3cca4 (feature)
Author: Andrea Testino <atestini@cisco.com>
Date:   Mon Feb 28 20:58:39 2022 -0500

    Added a line to the file this-is-a-test.txt

commit 72094085090e797d0148b5105b581e934779329f (origin/master, origin/HEAD)
Author: Andrea Testino <atestini@cisco.com>
Date:   Mon Feb 28 20:55:51 2022 -0500

    Adding empty file for later test

commit f82f85402b3606855e0d6669bc86cf922a6bd934
Author: aitestino <59578890+aitestino@users.noreply.github.com>
Date:   Mon Feb 28 20:48:41 2022 -0500

    Initial commit


ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ git branch -d feature
Deleted branch feature (was 1b5886c).

ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ git push origin master
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 451 bytes | 451.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/aitestino/DEVCOR-Git-Tests.git
   7209408..8d11c18  master -> master


ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ git log
commit 8d11c18b33c2cc8bd1a484a148a718683cdc891c (HEAD -> master, origin/master, origin/HEAD)
Merge: 7209408 1b5886c
Author: Andrea Testino <atestini@cisco.com>
Date:   Mon Feb 28 20:59:26 2022 -0500

    Testing --no-ff kw
    
    Merge branch 'feature'

commit 1b5886cb7cc25db5c400dc0ebcd07d1486a3cca4
Author: Andrea Testino <atestini@cisco.com>
Date:   Mon Feb 28 20:58:39 2022 -0500

    Added a line to the file this-is-a-test.txt

commit 72094085090e797d0148b5105b581e934779329f
Author: Andrea Testino <atestini@cisco.com>
Date:   Mon Feb 28 20:55:51 2022 -0500

    Adding empty file for later test

commit f82f85402b3606855e0d6669bc86cf922a6bd934
Author: aitestino <59578890+aitestino@users.noreply.github.com>
Date:   Mon Feb 28 20:48:41 2022 -0500

    Initial commit

ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ cat this-is-a-test.txt 
just changing some stuff here 123

ATESTINI-M-26WU:DEVCOR-Git-Tests atestini$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
```
