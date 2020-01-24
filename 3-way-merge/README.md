# Git Kata: 3-Way Merge

## Setup

1. Run `. setup.sh` (or `.\setup.ps1` in PowerShell)

## The task
You again live in your own branch, this time we will be doing a bit of juggling with branches, to show how lightweight branches are in git.

1. Create a branch called greeting and check it out
2. Edit the greeting.txt to contain your favorite greeting
3. Add greeting.txt files to the staging area
4. Commit
5. Switch back to the master branch
6. Create a file README.md with information about this repository
7. Add the README.md file to staging area and make the commit
8. What is the output of `git log --oneline --graph --all`?
	* 87bd25d (HEAD -> master) README.md
	| * ae24a52 (greeting) Initial commit
	|/  
	* 59937d5 Add content to greeting.txt
	* a62ee10 Add file greeting.txt

9. Diff the branches
	diff --git a/README.md b/README.md
	new file mode 100644
	index 0000000..ce01362
	--- /dev/null
	+++ b/README.md
	@@ -0,0 +1 @@
	+hello
	diff --git a/greeting.txt b/greeting.txt
	index c8fa032..ce01362 100644
	--- a/greeting.txt
	+++ b/greeting.txt
	@@ -1 +1 @@
	-Nihao
	\ No newline at end of file
	+hello

10. Merge the greeting branch into master
	Merge made by the 'recursive' strategy.
	 greeting.txt | 2 +-
	 1 file changed, 1 insertion(+), 1 deletion(-)

## Useful commands
- `git branch`
- `git branch <branch-name>`
- `git branch -d <branch-name>`
- `git checkout <branch-name>`
- `git checkout -b <branch-name>`
- `git branch -v`
- `git add`
- `git commit`
- `git commit -m`
- `git merge <branchA> <branchB>`
- `git diff <branchA> <branchB>`
- `git log --oneline --graph --all`
