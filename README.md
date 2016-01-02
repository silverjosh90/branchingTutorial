# Branching :herb:
:octocat: A short tutorial on the basics of branching with Git and Github 
###The real-life scenario:
Your boss has asked you to add a new button to the front page of their multi-million dollar companies website, you say "easy", but you want to do it safely without breaking the currently deployed site. That's where branching comes in...

###Fork and Clone
* :fork_and_knife::sheep:
  
###Get into the Terminal
* Let's get inside the directory `branchingTutorial` we just cloned.
* Inside there should be another directory titled `button1Feature`. `cd` into it.
* Now it's time to see what branching can do for us. 
* `$ git branch` will show us what branches we have at our disposal.
* *Note* The asterisk and/or highlighted branch is the branch you are ON.
* To make our new solution branch, type `$ git branch mySolution`. This will create a new branch titled "mySolution".
* *Note* Whenever you make a new branch, it will be a copy of the branch you are currently ON, not neccesarily a copy of `master`.
* `$ git branch` one more time to make sure that we see the new branch we just created. We should see
```
    * master
      mySolution
```
* `$ git checkout mySolution` will put us on our shiny new branch we just made.
* Open the `index.html` file in your browser so we can see the changes we are about to make.
![Button One](https://media.giphy.com/media/xghZ09m2CLTDa/giphy.gif)

###Add Feature
* Now that we are safely away from `master` on our `mySolution` branch, we can hack away and make changes fearlessly!
* Open the files in your favorite text editor with `$ atom .` or `$ sublime .`  etc.
* Let's add a new button that triggers an alert inside the `roundedBox` article. (if you need help with the code you can use the hidden branch 'solution'. `$ git checkout solution`)
* Our app should look something like this now.                
![Button Two](https://media.giphy.com/media/EdytL3UyLXBkY/giphy.gif)
* If so, let's commit and push! But remember, we are NOT pushing to `master`, we are pushing to `mySolution`. If we push to `master` we override everything and totally undermine our reason for branching. And your head implodes. :boom:

`$ git add -A`

`$ git commit -m "Feature button 2 complete"`

`$ git push origin mySolution`

* You have now have a safe feature branch and an untainted master up in the GitHub magic cloud! :clap:

###Next Steps
* Now if the changes were exactly what the boss wanted, you would merge your changes. Which is much more complicated when you are working with other developers, but for now, it's just lonesome ol' you, so you can safely merge your `master` branch and your `mySolution` branch.
* Go ahead and switch back to `master` with `$ git checkout master` so we can merge `mySolution` into it.
* Do the merge! `$ git merge mySolution`
* Now all the work we did in `mySolution` is part of `master`, and we don't need it anymore!
* After we have double checked to make sure that everything is working fine on `master`, let's blow up `mySolution`

`$ git branch -d mySolution`

###Celebrate!
* You've taken your first steps into a larger world...

![WooHoo!](https://media.giphy.com/media/ns8SCo6O6g7nO/giphy.gif)






