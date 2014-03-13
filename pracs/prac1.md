Welcome to Software Engineering 3: Testing & Quality
====================================================

The first prac is an introduction to git as a source control system.

Source control is a really important part of creating quality software, because it allows you to know who changed what and when, and by combining this with tests, it allows you to quickly identify which specific change(s) cause a test to fail.

Today you will:
  * Configure git in your CSEM computer account.
  * Create a github account.
  * Create a local git repository, and make multiple commits to it.
  * Create a git repository on github.
  * Push commits from a local repository to a remote repository hosted on github.
  * Pull commits from a remote repository to a local git repository.
  * Send a pull request to the owner of a repository, asking them to accept changes that you are proposing.
  * Use git to request that your checkpoint be marked off.

You must complete all actions to receive today's checkpoint.  If you can't get it finished today, that's okay, you have until the end of semester to complete the actions and receive your checkpoint.

This is a really important prac, because you will continue to use git to request that your checkpoints be marked off, and as you should know by now, they will form the entire (or in the case of GE students, the overwhelming majority) of your final grade.

If you spot any errors or omissions in this material, it is all stored in a git repository, so you can make the changes in a local copy of the repository, and send me a pull request asking me to accept the changes.

Following through the tasks below will allow you to complete the prac in a natural manner.

Configuring git in your CSEM computer account.
----------------------------------------------

Watch [this git introductory video](http://git-scm.com/video/get-going).  You may also wish to watch the [other videos in the series](http://git-scm.com/videos), they are all less than 10 minutes each.

Then use the git configure command to set your username and email address.  You should set your email address to your Flinders email address, so that I can easily match your work so that you get credit for it.

Useful resources for this step include:
  * [https://help.github.com/articles/setting-your-email-in-git](https://help.github.com/articles/setting-your-email-in-git)
  * [http://git-scm.com/book/en/Getting-Started-First-Time-Git-Setup](http://git-scm.com/book/en/Getting-Started-First-Time-Git-Setup)

Create a github account.
------------------------

If you don't already have a github account, go to [github.com](http://github.com) and create one.

As always, you should practice good password hygiene, and not use the same password as for any other service, including University systems.  **It is better to have strong passwords written on pieces of paper and secured in your physical wallet than to have weak passwords that might as well be written in plane sight for everyone to see**

Create a local git repository, and make multiple commits to it.
---------------------------------------------------------------

If you haven't already, it is probably a good idea to make a subdirectory in your home directory to hold all the files you will use for SE3.  We will use a number of directories over the semester, so I do encourage you to keep them all together somewhere.  My recommendation is that you create a directory called `se3` in your home directory, and then work from in there:

First, create the directory: `mkdir ~/se3`

Then change into that directory whenever you are doing SE3 work:  `cd ~/se3`

Now that you are in your SE3 directory, it's time to create your first git repository, which in a fit of imagination, we will call `prac1`:

Use this command: `git init prac1`

Using your favourite text editor, create a file called `README.md` in that directory.  From the command line, you could use `pico README.md` or if you are brave `vi README.md`.  

*Bravery has been called stupidity with a cause, where stupidity refers to taking actions that might cause you pain.  This is fair.  Learning to use the `vi` editor is brave, because the learning curve can be a bit painful.  But it is not without a cause, because `vi` is a powerful editor that is available on practically any computer system you might work on at the command-line level. Or at least all the interesting ones, anyway.  Using `vi` in this topic is safer than normal, because you will be learning how to use source control to be able to reverse any deadly mistakes that you make :)*

Whatever editor you choose, write a couple of lines of *publicly presentable* text into the file. I say publicly presentable, because this text will soon be visible to the entire world to read.  Be responsible.  When done, exit the editor.

Then tell git you would like to add the changes to that file to the next commit using the `git add` command:  `git add README.md`

This tells git that you want to record these changes.  The actual remembering happens with `git commit`, using a command like:  `git commit`

This should drop you into the `vi` editor.  Oh dear, even if you weren't planning on being brave, I have tricked you into it anyway.  Naughty me.

Here is all you need to know about vi for now:
  * If in doubt, press the escape (ESC) key a few times to make sure you are in command mode.
  * To begin typing, move the cursor somewhere, and then press `i` once to enter edit mode.  You can now type to your hearts content.  When done, press the escape (ESC) key to go back to command mode.
  * When you want to save and quit, press escape (ESC) a few times, and then two capital Z's.
  * If you want to quit without saving instead, press escape (ESC) a few times, and then type the following characters: `:q!` and press enter.  You will quit without saving.

With that in mind, `vi` should be running with a temporary file provided by git, asking you for a commit message, and telling you which files will be committed.  Write a one line message, perhaps along the lines of `my first commit`, save and exit `vi`.  Your commit has been recorded.

Next we will look at the history, and add another commit.

Edit your `README.md` file again.  It doesn't matter what you change.

Then repeat the `git add` and `git commit` commands above, putting an appropriate commit message in.

Now run `git log` and you should be able to see that git knows you have made two commits.

Create a git repository on github
---------------------------------

Log in to github using your git username, and create a new repository called `se3prac1`, using the web interface.

*This is probably a good time to go into "account settings" and then "SSH keys" on github, followed by "add key", and add the public key for your lofty account so that you can push changes to github without having to supply your github password every time.  You can find your public key in `.ssh/id_dsa.pub` on lofty.*

Once you have done all that, browse your new repository.  There will be a box titled `SSH clone URL`.  Copy that URL and use a command like: `git clone <that url>` from in your ~/se3 directory on lofty.  That will clone your new repository onto lofty.  You now have a local copy you can work on.

Push commits from a local repository to a remote repository hosted on github.
-----------------------------------------------------------------------------

Similar to before, create a file, and make some commits.  Use `git log` to verify that the commits were made.

Now look at the online page on github for your repository.  You won't see the commits there, because they only exist in your local repository on lofty right now.  This is a good thing.  It is what makes git usable when you are offline, for example, sitting in economy over the Pacific Ocean.

Now use `git push` to push those changes to github, and notice that they appear there.

Pull commits from a remote repository to a local git repository.
----------------------------------------------------------------

I'll write this in a moment.

Paul Gardner-Stephen, 13 March 2014.