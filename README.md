	Explain version control.
        This is a system that tracks the history of changes made to the code base (a file or set of files) as people and teams collaborate on projects together. The developers in this situation get to see the history of who changed what at any given time, and over time, specific versions can be recalled. A distributed version control system explains a situation whereby each developer can have a local copy of the project codebase independent of each other.


    Explain difference between git and github
        Git: Git is a free, open source tool for managing source code history. It is a distributed peer-to-peer version or revision control system for tracking changes in source code during software development. It is designed for coordinating work among programmers, but it can be used to track changes in any set of files with a unified goal of speed, data integrity, and support for distributed, non-linear workflows.
        GitHub: GitHub is a web-based hosting service for Git repository. This offers all of the distributed revision control and source code management (SCM) functionality of Git as well as adding its own features. It provides access control and several collaboration features such as wikis, task managemnt and bug tracking and feature requests for every project.
        PS: You do not need GitHub to use Git


    List 3 other github alternatives
        itLab
        Bitbucket
        GitBucket
        AWS CodeCommit
        Sourceforge
        Google Cloud Source Repositories
        Phabricator


    Explain the difference between git fetch and git pull,
        git fetch: this gathers any commits from the target branch or remote repository that do not exist in the current branch and stores them in the local repository without bringing the changes into the working directory. However, it does not merge them with your current branch. This is particularly useful when it comes to keeping the repository up to date. To integrate the commits into your current branch, you must use git merge afterwards.
        git pull: this automatically merge after fetching commits (all changes) from the remote directory changes into the working directory. It is context sensitive, so all pulled commits will be merged into the currently active branch. git pull automatically merges the commits without giving the chance to review them first. This may result into running into frequent conflicts if the branches are not carefully managed.

        
    Explain in simple terms git rebase and the command for it
        This is one of the ways to integrate changes from one branch into another. With the rebase command, all the changes that were committed on one branch can be replayed on a different branch. The Git rebase command moves a branch to a new location at the head of another branch - combining two source code branches into one.

        First, check that the master branch has no outstanding changes.
        git status
    
        Checkout the new-feature branch.
        git checkout new-feature
    
        Tell git to rebase the current branch onto the master branch.
        git rebase master
    
        Confirm that there are two branches.
        git branch
    
        Swap back to the master branch
        git checkout master
    
        We merge the new-feature branch into the current branch, which in our case is the master branch.
        git merge new-feature


    Explain in simple terms git cherry-pick and the command for it
        git cherry-pick is a command that allows the developer to apply the changes made by specific commits from any branch to the current branch. In simple term, cherry picking is the act of picking a commit from a branch and applying it to another. This can be useful for undoing changes or moving commits to the correct branch. Unlike git merge or git rebase, which integrate all commits from one branch, git cherry-pick allows the selection of individual commits for integration.

        Command:
    
        Commit hash
            git log --oneline
    
        cherry-pick command
            git cherry-pick <commitSha>
            Where commitSha is a commit reference
    
        Add commit changes to the working copy
            git cherry-pick 65be1e5 --no-commit
    
        Select more than one commit simultaneouly
            git cherry-pick hash1 hash3
