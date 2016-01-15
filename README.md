## Objectives

  1. Know when a knew model class method is needed
  2. Create Class Model methods that act like scopes

## Overview

Blog example still. Pull the code from the last reading so that students can follow along! This one is going to be a codealong. So write tests for the finished "product" with the filtering and everything. On clone the tests shouldn't pass, but by copy/pasting everything in this reading they'll get it to pass. Put in a db/seeds that gets eneough seeded data to make it interesting

  * Sometimes you want to do some filtering of your posts. Let's make it so we can get Today's posts, Yesterday's posts. Or Let's filter by Author.
  * All logic in views (feel the pain) Use the `params` hash in the view just to exaggerate things a bit. You can do that by doing this http://stackoverflow.com/a/20164155
    * Create drop down for artist and date (just today/yesterday)
    * Submit button that reloads the page with filter applied. 
    * Woah that feels icky. Doing so much in views
    * Where do we want to refactor this out?
      * First try bringing it to the controller.
      * With the controller it's still icky. The controller is reaching around the model to get straight to the DB. bad!
      * Let's move it to model methods
  * Model method. Class or Instance? (I know that is obvious but it's a hard concept. always can use repeating)
    * Since we are operating on all of the instances of the model it can't be an instance method, must be class method
    * Write the class methods to look like [this](https://github.com/learn-co-curriculum/arel-lab/blob/4d50ff04c7724d598efb4283b964ec45903c54fd/app/models/boat.rb#L23) That is the following lab so I wanna give them a fighting chance
  * Refactor the views to use your new class methods without params in the views. So much better


