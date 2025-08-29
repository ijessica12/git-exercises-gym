# Git Exercises
## Bundle 1
### Exercise 1
`````bash
CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise
$ git init
Initialized empty Git repository in C:/Users/CMU/Desktop/git/exercise/.git/

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ echo "hello world"> hello.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git checkout master
error: pathspec 'master' did not match any file(s) known to git

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git checkout -b master
Switched to a new branch 'master'

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (master)
$ git checkout main
error: pathspec 'main' did not match any file(s) known to git

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (master)
$ git checkout -b main
Switched to a new branch 'main'

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git add hello.html
warning: in the working copy of 'hello.html', LF will be replaced by CRLF the next
time Git touches it

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git commit -m "init the commit"
[main (root-commit) 231fe03] init the commit
 1 file changed, 1 insertion(+)
 create mode 100644 hello.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git remote add origin git@github.com:ijessica12/git-exercises-gym.git

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git remote -v
origin  git@github.com:ijessica12/git-exercises-gym.git (fetch)
origin  git@github.com:ijessica12/git-exercises-gym.git (push)

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 226 bytes | 113.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:ijessica12/git-exercises-gym.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git checkout -b dev
Switched to a new branch 'dev'

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (dev)
$ git checkout -b test
Switched to a new branch 'test'

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (test)
$ git checkout dev
Switched to branch 'dev'

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (dev)
$ git checkout -d test
HEAD is now at 231fe03 init the commit

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise ((231fe03...))
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/ijessica12/git-exercises-gym/pull/new/dev
remote:
To github.com:ijessica12/git-exercises-gym.git
 * [new branch]      dev -> dev

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise ((231fe03...))
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

`````

### Exercise 2
`````bash
CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ touch home.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ code home.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git add home.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git commit -m "init commit to the home"
[main 741fd62] init commit to the home
 1 file changed, 14 insertions(+)
 create mode 100644 home.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ echo "you can find us on ">>home.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git stash
warning: in the working copy of 'home.html', LF will be replaced by CRLF the next t
ime Git touches it
Saved working directory and index state WIP on main: 741fd62 init commit to the hom
e

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git stash list
stash@{0}: WIP on main: 741fd62 init commit to the home

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ echo "about us ">about.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git add about.html
warning: in the working copy of 'about.html', LF will be replaced by CRLF the next
time Git touches it

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git commit -m " init commit to the about page"
[main feb73da]  init commit to the about page
 1 file changed, 1 insertion(+)
 create mode 100644 about.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ echo "contact us ">>about.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git stash
warning: in the working copy of 'about.html', LF will be replaced by CRLF the next
time Git touches it
Saved working directory and index state WIP on main: feb73da  init commit to the ab
out page

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ echo "our team members">team.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git add team.html
warning: in the working copy of 'team.html', LF will be replaced by CRLF the next t
ime Git touches it

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git commit -m "init commit to the team page"
[main c91f0c9] init commit to the team page
 1 file changed, 1 insertion(+)
 create mode 100644 team.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ echo "team1 team2 team3 team 4">>team.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git stash
warning: in the working copy of 'team.html', LF will be replaced by CRLF the next t
ime Git touches it
Saved working directory and index state WIP on main: c91f0c9 init commit to the tea
m page

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git stash list
stash@{0}: WIP on main: c91f0c9 init commit to the team page
stash@{1}: WIP on main: feb73da init commit to the about page
stash@{2}: WIP on main: 741fd62 init commit to the home

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git stash pop stash@{1}
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   about.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Readme.md

no changes added to commit (use "git add" and/or "git commit -a")
Dropped stash@{1} (657f6587d96ea0775dc3f5cf5572e822b8247673)

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git stash pop stash@{1}
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   about.html
        modified:   home.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Readme.md

no changes added to commit (use "git add" and/or "git commit -a")
Dropped stash@{1} (055da99bfdf001209a7f4ec2117b646386f340bf)

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git add about.html home.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git commit -m "restore about page and home page using stash"
[main e353073] restore about page and home page using stash
 2 files changed, 2 insertions(+), 1 deletion(-)

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git push origin main
Enumerating objects: 14, done.
Counting objects: 100% (14/14), done.
Delta compression using up to 4 threads
Compressing objects: 100% (10/10), done.
Writing objects: 100% (13/13), 1.31 KiB | 335.00 KiB/s, done.
Total 13 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
To github.com:ijessica12/git-exercises-gym.git
   231fe03..e353073  main -> main

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git stash pop
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   team.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Readme.md

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (692ca28deff1f1925514e09ce7e0e54ee9579e8e)

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git reset
Unstaged changes after reset:
M       team.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git restore team.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git status -s
?? Readme.md
`````

## Bundle 2
### Exercise 1
````` bash
CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/bundle-2)
$ echo "our services">services.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/bundle-2)
$ git add services.html
warning: in the working copy of 'services.html', LF will be replaced by CRLF the ne
xt time Git touches it

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/bundle-2)
$ git commit -m "init the commit service page"
[ft/bundle-2 3b63d92] init the commit service page
 1 file changed, 1 insertion(+)
 create mode 100644 services.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/bundle-2)
$ git push -u origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 293 bytes | 293.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/ijessica12/git-exercises-gym/pull/new/ft/bundle-2
remote:
To github.com:ijessica12/git-exercises-gym.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$
`````

### Exercise 3
`````bash
CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/service-redesign)
$ echo "Here are our services We provide top-notch services for our clients">services.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/service-redesign)
$ git add services.html
warning: in the working copy of 'services.html', LF will be replaced by CRLF the ne
xt time Git touches it

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/service-redesign)
$ git commit -m "modify our service page"
[ft/service-redesign d41cdba] modify our service page
 1 file changed, 1 insertion(+)
 create mode 100644 services.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/service-redesign)
$ git push -u origin ft/service-redesign
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 334 bytes | 55.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/ijessica12/git-exercises-gym/pull/new/ft/service-re
design
remote:
To github.com:ijessica12/git-exercises-gym.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ echo "visit us">services.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git add services.html
warning: in the working copy of 'services.html', LF will be replaced by CRLF the ne
xt time Git touches it

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git commit -m "redesign services page"
[main f5595ec] redesign services page
 1 file changed, 1 insertion(+)
 create mode 100644 services.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git pull origin main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 897 bytes | 2.00 KiB/s, done.
From github.com:ijessica12/git-exercises-gym
 * branch            main       -> FETCH_HEAD
   e353073..fed0cd5  main       -> origin/main
Auto-merging services.html
CONFLICT (add/add): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main|MERGING)
$ git add services.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main|MERGING)
$ git commit -m "resolving merge issue"
[main be725c8] resolving merge issue

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git push origin main
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 583 bytes | 72.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To github.com:ijessica12/git-exercises-gym.git
   fed0cd5..be725c8  main -> main

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/service-redesign)
$ git diff main
diff --git a/services.html b/services.html
index 30e19c8..cd52e24 100644
--- a/services.html
+++ b/services.html
@@ -1,2 +1 @@
-visit us
-our services
\ No newline at end of file
+Here are our services We provide top-notch services for our clients

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/service-redesign)
$ git add service.html
fatal: pathspec 'service.html' did not match any files

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/service-redesign)
$ git add services.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/service-redesign)
$ git commit -m "REsolve conflict between main and ft/service-redesign branch"
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Readme.md

nothing added to commit but untracked files present (use "git add" to track)
`````
## Bundle 3
### Exercise 1
`````bash
CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/team-page)
$ echo "number of team  we have">teams.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/team-page)
$ git add teams.html
warning: in the working copy of 'teams.html', LF will be replaced by CRLF the next
time Git touches it

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/team-page)
$ git commit -m "adding team we have"
[ft/team-page a08d40e] adding team we have
 1 file changed, 1 insertion(+)
 create mode 100644 teams.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/team-page)
$ git push -u origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 304 bytes | 304.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/ijessica12/git-exercises-gym/pull/new/ft/team-page
remote:
To github.com:ijessica12/git-exercises-gym.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/team-page)
$ git log
commit a08d40ebd89bdc049299c231ad88ef85ddac19b0 (HEAD -> ft/team-page, origin/ft/te
am-page)
Author: Jessica <ishimwejessica2@gmail.com>
Date:   Fri Aug 29 23:40:48 2025 +0200

    adding team we have

commit be725c86b28034be5ce0618f7d7e2b19453f05d3 (origin/main, main, ft/contact-page
)
Merge: f5595ec fed0cd5
Author: Jessica <ishimwejessica2@gmail.com>
Date:   Fri Aug 29 23:16:46 2025 +0200

    resolving merge issue

commit f5595ecff33720aa389b32e783ea65f7f45f35ad
Author: Jessica <ishimwejessica2@gmail.com>
Date:   Fri Aug 29 23:04:03 2025 +0200

    redesign services page

commit fed0cd5b28867abecf05c0fa834a88e1c7cd6ea0
Merge: e353073 3b63d92
Author: Jessica ISHIMWE <ishimwejessica2@gmail.com>
Date:   Fri Aug 29 21:14:31 2025 +0200

    Merge pull request #1 from ijessica12/ft/bundle-2

    service

commit 3b63d922ff3042da379ab927d722d402baf9aa08 (origin/ft/bundle-2, ft/bundle-2)
Author: Jessica <ishimwejessica2@gmail.com>
Date:   Fri Aug 29 21:12:32 2025 +0200

    init the commit service page

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/contact-page)
$ git cherry-pick a08d40ebd89bdc049299c23
[ft/contact-page 16fd288] adding team we have
 Date: Fri Aug 29 23:40:48 2025 +0200
 1 file changed, 1 insertion(+)
 create mode 100644 teams.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/contact-page)
$ touch contact.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/contact-page)
$ code contact.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/contact-page)
$ git add contact.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/contact-page)
$ git commit -m "add contact page"
[ft/contact-page e69c437] add contact page
 1 file changed, 18 insertions(+)
 create mode 100644 contact.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/contact-page)
$ git push -u origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 770 bytes | 20.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/ijessica12/git-exercises-gym/pull/new/ft/contact-pa
ge
remote:
To github.com:ijessica12/git-exercises-gym.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/faq-page)
$ touch faq.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/faq-page)
$ code faq.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/faq-page)
$ git add faq.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/faq-page)
$ git commit -m "adding faq page"
[ft/faq-page 766f113] adding faq page
 1 file changed, 16 insertions(+)
 create mode 100644 faq.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/faq-page)
$ git push -u origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 486 bytes | 486.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/ijessica12/git-exercises-gym/pull/new/ft/faq-page
remote:
To github.com:ijessica12/git-exercises-gym.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/faq-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/team-page)
$ git revert a08d40ebd89bdc049299c231
[ft/team-page 8ee1cfe] Revert "adding team we have"
 1 file changed, 1 deletion(-)
 delete mode 100644 teams.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/team-page)
$ git push -u origin ft/team-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 251 bytes | 251.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:ijessica12/git-exercises-gym.git
   a08d40e..8ee1cfe  ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
`````

### Exercise 2
`````bash
CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/team-page)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'
Your branch is up to date with 'origin/ft/faq-page'.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ code home.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git add home.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git commit -m "modify home page"
[main 24ae859] modify home page
 1 file changed, 3 insertions(+), 1 deletion(-)

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 401 bytes | 401.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:ijessica12/git-exercises-gym.git
   be725c8..24ae859  main -> main

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/home-page-redesign)
$ git add home.html

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/home-page-redesign)
$ git commit -m "redesign home page"
On branch ft/home-page-redesign
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Readme.md

nothing added to commit but untracked files present (use "git add" to track)

CMU@DESKTOP-DGCLDK7 MINGW64 ~/desktop/git/exercise (ft/home-page-redesign)
$ git push -u origin ft/home-page-redesign
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 4 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (9/9), 1.08 KiB | 555.00 KiB/s, done.
Total 9 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/ijessica12/git-exercises-gym/pull/new/ft/home-page-
redesign
remote:
To github.com:ijessica12/git-exercises-gym.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

`````