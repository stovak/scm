!SLIDE
# What is SCM?
  
  - Source Control Management, AKA version control
  - Allows teams of developers to work on code simultaneously and manages the revisions
  - Provides historical record of who fucked things up
  - Provides backend repeatable way to deploy code

!SLIDE
  
# Examples of SCM

  - Open: CVS, GIT, SVN (SubVersioN), Mercurial
  - Propriatary: Vault, Perforce
  - Cloud-based services: Github, Beanstalk, SourceSafe (M$ specific), Bitbucket
  
!SLIDE

#Distributed VS Centralized
  - Centralized:
    - CVS, SVN has a centrilized structure
    - You commit to the centralized repo
  - Distributed:
    - Git is distributed
    - You can have multiple remotes
    - You can have multiple "forks" (more on "forks" later)
    - You commit locally then "push" that commit to the remote(s)

!SLIDE
  
# 300 lb gorilla
  - https://github.com
  - 3 Million + active developers
  - Robust API
  - it just works
  - Site search as well as google search integration for your repo
  - "Sourceforge done right"
  
!SLIDE
    
# Definitions
  - Repository(repo): The place where a versioned project is kept.
  - Working Folder: A local copy of the (usually) remote repository
  - Checkout/Clone: The action of referencing the repo locally so as to make changes
  - Fork: To copy a repo for the purposes of using the code in a different way
  - Pull Request: From the forked repo, request that your changes to the fork be incorporated into the original
  - Master/Trunk: for git repos, every repo has a master. In SVN, it's called a trunk. It's the origin of life for the repo.
  - Branch: slightly different version of the Master with changes that have yet to be approved/used/implemented
  - Merge: Take code in a branch and combined it with the master retaining the pertinent changes
  - Tags: You can tag commits for reference: "v1.0", "prod on april 15", etc 
  - Commit hooks: Actions that are performed when commits are checked in or pushed to remote
  
!SLIDE
  
# Basic Workflow
  - copy code to local working folder
  - make changes to working code
  - create a commit of your changes with a description
  - merge your commit back to the remote
  - ABCP: Always be committing & pushing
    - Teach yourself to enforce good code practices
    - Share as much code as the project allows
  
!SLIDE
  
# More complicated Workflow
  - Branch remote for your new feature
  - Clone the branch locally
  - Make changes and check your changes into the branch
  - Real developers never test their code. It's always right the first time
  - push the branch out to remote
  - Build a copy of the project for QA based on the branch
  - Merge the branch into the master
  - Tag the merge-commit as "Version x" to indicate a release.

!SLIDE

#Deployment
  - for iOS/Android apps not really an issue
  - for webapps, you have a prod, stage, and dev branch
  - each represents the code in your three website environments
  - merge with the dev branch and trigger a dev build with post-commit hook
  - merge dev with stage and trigger post-commit hook
  - merge stage with master and trigger post-commit hook
  
!SLIDE
  
# GUI vs Command Line
  - Tower.app(git), Gitx(git), Versions(svn), Cornerstone(svn)
  - Real programmers use the command line
  
!SLIDE
  
# XCode
  - Git/SVN integration is "usable"
  - More robust GUI's available (e.g. Tower.app)
  - Real programmers use the command line
  
!SLIDE

# Student Exercise
  - Install GIT on your machine from http://git-scm.com
  - Go to https://github.com and create a user for yourself.
  - Follow the instructions on the created repo to push your first commit out
  
!SLIDE

# Team Exercise
  - I will create a Repo with a "student list"
  - Students fork the repo
  - Students update "student list" with their name/email
  - Students create Pull request for me to incorporate their changes
  
!SLIDE

#Takeaway Excercise
  - I will incorporate the pull request commits
  - Update your fork with the latest changes from the upstream master

