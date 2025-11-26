Vocabulary + Mental Model

---

## 1. Working Tree
the working tree is the actual files you see and edit on your machine.

if you open VS Code and modify app.py, that’s the working tree changing.  
nothing here is stored in Git yet.

---

## 2. Index (Staging Area)
the index is a snapshot waiting room.

when you run git add, your file is copied into a temporary staging snapshot.  
commit only saves what’s in the index, not what’s in the working tree.  
Staging = intentional control over what enters history.

---

## 3. Local Repository
inside .git/ is your entire Git history: commits, objects, branches, reflogs.

local = on your machine.  
remote = on GitHub or any server.  
your real repo is .git.

everything outside it is just the working tree.

---

## 4. Remote Repository
a remote is simply a URL that hosts another copy of your repo.

GitHub is not Git.  
GitHub is hosting your Git repo and providing UI + services.  
origin = the default name of the remote repo.

---

## 5. Blob
Blob = raw file content stored by Git.

Git does not store filenames inside blobs, just content.

---

## 6. Tree
Tree = directory structure.

a tree stores filenames, modes, and pointers to blobs/other trees.  
Tree = folder snapshot.

---

## 7. Commit
a commit is a pointer to a tree, plus:

• parent commit(s)  
• author  
• message  
• timestamp  

every commit creates a new state of your project.  
Commit = the fundamental unit of your project history.

---

## 8. Tag
a tag is a named pointer to a commit.

think release versioning: v1.0.0.  
annotated tags store metadata.  
lightweight tags only store a pointer.

---

## 9. Branch
a branch is just a file containing a commit hash.

nothing more.  
it just points to the commit.  
this is why creating a new branch feels fast enough. no copy of whole repo occurs, just new commit occurs and points to that commit

Branch = a moving pointer into your commit graph.

---

## 10. HEAD
HEAD tells Git where you are right now.

usually points to a branch.  
sometimes directly points to a commit (detached HEAD).  
HEAD = your current position in history.

---

## 11. Remote-tracking Branch
a read-only branch that shows the last known state of the remote.

Example: origin/main.  
It’s NOT the remote branch, it’s your local copy of it.

---

## 12. Detached HEAD
you’re on a commit, not a branch.

this means commits you make don’t belong to any branch until you attach one.

---

## 13. Untracked File
a file Git has never seen.

Not staged. Not committed.

---

## 14. Modified File
a tracked file that changed in the working tree.

---

## 15. Staged File
a file whose changes are stored in the index.

---

## 16. Committed File
the file snapshot is recorded in the repository’s history.

---

## 17. Ignored File
files Git intentionally never tracks.

Controlled by .gitignore

---

## 18. init
creates a new local Git repo by generating the .git directory.

---

## 19. clone
copies an existing remote repo to your machine and sets origin.

---

## 20. add
moves changes from working tree → index.

---

## 21. commit
converts the staged snapshot into a commit object.

---

## 22. status
shows file states: untracked, modified, staged.

---

## 23. diff
shows line-by-line differences between two areas.

---

## 24. log
displays commit history.

---

## 25. branch
breates or lists branches.

---

## 26. checkout / switch
switches branches or restores files.

switch = safer version  
checkout = older but more powerful.

---

## 27. merge
combines two branches.

can be:  
• fast-forward  
• 3-way merge  
• conflict-producing merge

---

## 28. rebase
moves commits onto a new base.  
creates new commits (history rewrite).

---

## 29. stash
temporarily saves uncommitted changes without a commit.

---

## 30. revert
creates a new commit that undoes another commit.

---

## 31. reset
moves HEAD/branch pointers backward.  
- can rewrite history.

---

## 32. push
send local commits to the remote repository.

---

## 33. pull
fetch + merge.  
gets remote changes and integrates them.

---

## 34. fetch
gets remote changes but does not merge them.

---

## 35. Snapshot Model
git stores snapshots of files, not diffs.  
commits point to full trees of files.

---

## 36. Hash / SHA-1
object identity is determined by hashing its contents.  
change any byte = new hash.

---

## 37. Parent Commits
every commit references its previous one(s).  
this forms a graph.

---

## 38. History Graph
git history is not a list, it’s a directed acyclic graph.  
this makes branching trivial.

---

## 39. Fast-forward
when a branch pointer can move forward without creating a merge commit.

---

## 40. Merge Commit
a commit with two parents.

---

## 41. Rewriting History
creating new commits while replacing older ones.  
examples: rebase, reset –hard.

---

## 42. Conflicts
when Git cannot automatically merge or rebase changes.  
- errors.

---

## 43. Reflog
Git’s private log of HEAD movements.  
- this is your undo-safety-space.

---

## 44. .git Directory
the real Git repo.

contains:  
• objects  
• refs  
• HEAD  
• logs  
• index  
• config

---

## 45. refs
references to commits (branches, tags, remotes).  
- stored in .git/refs/.

---

## 46. origin
default name for the remote repository.

---

## 47. upstream Branch
the default branch your local branch compares against.

used for pull/push without specifying names.

---

these are the main terms necessary for better conceptual, and under-hood understanding of git 101 series.

you can read the series of [@blogs](https://yswnth.bearblog.dev) in here. and i do write a lot in twitter [@yswnth](https://x.com/yswnth)

Tomorrow : Day 01/13 of Git 101 Series : What Git actually is?
