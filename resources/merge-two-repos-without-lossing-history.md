# How to Merge Repost Without Losing History (without using submodules) :blue_book:
If you want an old project(repo) to be a subdirectory of a new project  such is the case here in GDI where we want to merge individual curriculum topics into the master curriculum repository, use this guide to help you.

Background:
While developing the master curriculum repository, I wanted to merge one of the individual html-css intro repository into it but without losing the history. Most of the resources I found online, suggest using [submodules](https://stackoverflow.com/questions/1425892/how-do-you-merge-two-git-repositories) which goal is to bring in source code from external libraries or projects and where you want to suggest or shop changes to bring back to them and the whole process is kind of complex.

The good news is that Git provides an easier alternative to accomplish this task. Our goal is to connect two repositories together and have them look as they had always being in one repository, and we don't want to lose the individual project history in the process and neither in this case trying to make changes or ship things back to the individual old repository and instead from now on to maintain all the code here in the master curriculum while keeping the fill log of the old repository which is useful so we can understand why things were done that way they are.

---

## Steps:
* Step 1: Clone projects:
    ```
  git clone git@github.com:girldevelopit/GDI-Master-Curriculum.git
  git clone git@github.com:girldevelopit/old-individual-project.git
  ```

* Step 2: Moving old repo to master curriculum:
  ```
  cd old-individual-project
  mkdir old-individual-project
  git mv !(old-individual-project) old-individual-project
  git add .
  git commit -m “Moving old project into its own subdirectory to prepare for merge to GDI master curriculum”
  git push
  ```
  !(old-individual-project) is a shell command that says “everything but old-project”. If your project is called html-css, then you move “everything but the html-css.

  Troubleshooting :information_desk_person: :bulb:: When you are moving the files, if you encounter the following error like this one:
  ```
  -bash: !: event not found
  ```
  Run the following command:
  ```
  $ shopt -s extglob; set +H
  ```
  The !(old-individual-project) shell command is an extended glob and extglob is turned off so by running the command above, it should fix the event not found error.  [More info](https://askubuntu.com/questions/798749/bash-event-not-found)

* Step 3: Merging
  ```
  # Go to the GDI Master Curriculum folder
  cd ../GDI-Master-Curriculum

  # Add a remote for and fetch the old repo
  git remote add -f old-individual-project <old-individual-project repo URL>

  # Merge the files from old_a/master into new/master
  git merge -S --allow-unrelated-histories old-individual-project/master


  git push origin feature/merge-old-individual-project
  git remote rm old-individual-project
  ```


  **git checkout -b feature/merge-old-individual-project**
  What we’re doing is add a remote to the old project, and merge everything into the GDI-Master-Curriculum. Since git doesn’t allow merges without a common history, we’ll have to force it using the allow-unrelated-histories option. Because there is a good practice to have a well maintained repo, we’re doing everything in a branch which we will merge after a code review is done.

## Conclusion:
By doing few normal merges, we are able to merge two repositories together into the GDI master curriculum repo and make it look like it was that way all along.  Avoid headaches using submodules or subtree merges.
