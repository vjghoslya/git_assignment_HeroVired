# git_assignment_HeroVired

=======================================
Question 1.
1. git clone git@github.com:vjghoslya/git_assignment_HeroVired.git

2. git checkout -b dev
3. Create python script calculator.py
4. git add .
5. git commit -m "dev to dev"
6. git push origin dev

7. git checkout main
8. git merge dev

9. git push origin main
10. git tag v1.0
11. git push origin v1.0

12. At Github UI, click(git_assignment_HeroVired) --> Tags --> select v1.0 --> Create Release --> Done

13. git checkout -b feature/sqrt
14. Add feature/sqrt code in calculator.py
15. git add .
16. git commit -m "commit from freature branch"
17. git checkout dev
18. Add emergency fix in  .\calculator.py

19. git commit -m "error fixed devide by 0 bug"

20. git push origin dev

21. create a pull request targeting the main branch.

21. git checkout feature/sqrt

22. git merge dev

23. git push origin feature/sqrt

24. At Github UI, create a pull request targeting feature/sqrt to the dev branch. and approve it from review approver.
25. At Github UI, create a pull request targeting from dev to the main branch. and approve it from review approver.

24. git checkout main

25. At Github UI, click(git_assignment_HeroVired) --> Tags --> select v1.0 --> Create Release --> Done
27. git pull origin main
28. git tag v2.0
29. git push origin v2.0

=======================================
Question 2.
At source machine


dnf install git-lfs

root@ip-172-31-0-136:/Operations# git clone git@github.com:vjghoslya/git_assignment_HeroVired.git
root@ip-172-31-0-136:/Operations# cd git_assignment_HeroVired/
root@ip-172-31-0-136:/Operations/git_assignment_HeroVired# ll
total 20
drwxr-xr-x 3 root root 4096 Feb 27 00:44 ./
drwxr-xr-x 3 root root 4096 Feb 27 00:44 ../
drwxr-xr-x 8 root root 4096 Feb 27 00:44 .git/
-rw-r--r-- 1 root root   26 Feb 27 00:44 README.md
-rw-r--r-- 1 root root  801 Feb 27 00:44 calculator.py
root@ip-172-31-0-136:/Operations/git_assignment_HeroVired# git checkout -b lfs
Switched to a new branch 'lfs'
root@ip-172-31-0-136:/Operations/git_assignment_HeroVired#

root@ip-172-31-0-136:/Operations/git_assignment_HeroVired# dd if=/dev/zero of=largefile.bin bs=1M count=300

root@ip-172-31-0-136:/Operations/git_assignment_HeroVired# git lfs track "*.bin"
Tracking "*.bin"

git add .gitattributes largefile.bin

git commit -m "Added large file using Git LFS"

git push origin lfs

------

At another machine

git checkout -b lfs
git pull origin lfs

======================================================
Question 3.

git checkout -b geometry-calculator
git checkout -b feature/circle-area
create GeometryCalculator.py and enable Circle-area code 
git add .
git stash push -m "WIP: Circle area feature in progress"
git status
list directory using 'ls' command.

git checkout -b feature/rectangle-area
edit GeometryCalculator.py and disable Circle-area code and enable Rectange-area code
git add .
git stash push -m "WIP: Rectangle area feature in progress"
git status

Switch back to the circle area branch and apply stashed changes
git checkout feature/circle-area
git stash list
git stash pop "stash@{1}" 
git add .
git commit -m "Feature Added : Circle Area Calculation"
git push origin feature/circle-area

Switch back to the rectangle area branch and apply stashed changes
git checkout feature/rectangle-area
git stash list
git stash pop "stash@{0}" 
git add .
git commit -m "Feature Added : Rectangle Area Calculation"
git push origin feature/rectangle-area

Create pull requests
Open GitHub URL
Create a pull request from feature/circle-area to dev. Add any of your classmate and reviewer.
Create a pull request from feature/rectangle-area to dev. Add any of your classmate and reviewer.

Once reviewer/approver approve the pull request. Merge each requests from dev branch to main branch.
