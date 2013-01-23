Overview
========

Welcome to the [Scrappy Academy](http://scrappyacademy.com/)

We're a Ruby (and Rails) self study group that meets weekly. Our goal is to expand our knowledge of the Ruby programming
language; as well as dive into the Rails web framework now and then.

If you are interested in joining us we please reach out. Our contact information is below and we communicate heavily
via the Google Group.

Join Us
-------

  * Google Groups: https://groups.google.com/d/forum/scrappyacademy
  * GitHub: https://github.com/ScrappyAcademy
  * Twitter: [Sir Scrappy](https://twitter.com/scrappyacademy)
  * Campfire: https://scrappyacademy.campfirenow.com/login


Learning Ruby
=============


### TODO

  [ ] Add books
  
  [ ] Add learning order (including Eloquent and POODR)
  
  [ ] Add code school links (Try Ruby and Git both free)
  
  [ ] Checklist of skills (find other git based programmer checklist)
  
  [ ] Add Tapas link


There are lots of resources for learning Ruby. The following are just some that we have found useful and recommend to new members.

  * [Quickstart](http://www.ruby-lang.org/en/documentation/quickstart/)
  * [Ruby from Other Languages](http://www.ruby-lang.org/en/documentation/ruby-from-other-languages/)
  * [Eloquent Ruby](http://www.amazon.com/Eloquent-Ruby-Addison-Wesley-Professional-Series/dp/0321584104/) by Russ Olsen
  * [Practical Object-Oriented Design in Ruby](http://www.amazon.com/Practical-Object-Oriented-Design-Ruby-Addison-Wesley/dp/0321721330/) by Sandi Metz
  * [Ruby Koans](http://rubykoans.com/) [on github](https://github.com/edgecase/ruby_koans) _we
    highly recommend using this as a learning tool_
  * [Ruby in 100 Minute](http://tutorials.jumpstartlab.com/projects/ruby_in_100_minutes.html)
  * [The Bastards Book of Ruby](http://ruby.bastardsbook.com/)
  * [Programming Ruby](http://ruby-doc.org/docs/ProgrammingRuby/html/intro.html)
    * This is a free online resource, though it is written for 1.8 it is becoming more outdated
    * The updated reference is available for purchase as [The Pickax Book](http://pragprog.com/book/ruby3/programming-ruby-1-9)
    * This is a really good reference book, but is a bit dense and may not be the best introduction point
  * [Ruby Quick Reference](http://www.zenspider.com/Languages/Ruby/QuickRef.html)
  * [Ruby Quiz](http://www.rubyquiz.com/)

In general, prag prog (http://pragprog.com) is a great resource (if you can spare the $$) for learning. If you are unsure of a book just ask. I'm sure someone has read (or will be reading it).

TODO: note about Ruby Koans as yu go through other things


Misc Tutorials
--------------

  * [RVM](http://tutorials.jumpstartlab.com/topics/environment/rvm.html)
  * [Bundler](http://tutorials.jumpstartlab.com/topics/environment/bundler.html)
  * Rspec
    * [RSpec and BDD](http://tutorials.jumpstartlab.com/topics/internal_testing/rspec_and_bdd.html)
    * [RSpec Practices](http://tutorials.jumpstartlab.com/topics/internal_testing/rspec_practices.html)


Podcasts
--------

TODO


Learning Rails
==============

A great Rails resource is http://railscasts.com/. I use it all the time.

TODO

Misc Tutorials
--------------

  * [Heroku](http://tutorials.jumpstartlab.com/topics/environment/heroku.html)


Git & GitHub
============

We're using [github](http://github.com) for all of our source code hosting. To get started and join the fun:

  1. [Create a _free_ github account](https://github.com/signup/free)
  2. [Contact us](#contact%20us) and request to join the group

Tutorials & Books
-----------------

  * [Try GitHub](http://try.github.com)
  * [Pro Git](http://git-scm.com/book) (_free online_)
  * [Common Git Practices](http://tutorials.jumpstartlab.com/topics/environment/git_strategy.html)
  * [Git Immersion](http://gitimmersion.com/)

Workflow Opinions
-----------------

  * [GitHub Flow](http://scottchacon.com/2011/08/31/github-flow.html)
  * [How GitHub Works](http://zachholman.com/posts/how-github-works/)
  * [How GitHub Uses GitHub to Build GitHub](http://youtu.be/MQZoy3VU3io?hd=1)
  * [Product Design](http://warpspire.com/posts/product-design/)
  * [Pull Requests 2.0](https://github.com/blog/712-pull-requests-2-0)

Our Workflow
------------

Since the team is largely distributed and needs to work asynchronously,
the [GitHub workflow](http://scottchacon.com/2011/08/31/github-flow.html)
seems the best fit to meet these needs. The workflow boils down to:

  * Everyone has full access
  * Use the [campfire chatroom](https://scrappyacademy.campfirenow.com)
    * This provides a central location for communications
    * It serves as a living transcript of our process
  * Anyone can pull any story to work on
  * Pair programming is highly encouraged (thus multiple people can work on the same story)
  * Master is **_always_** deployable
  * Keep branches simple

This is the base foundation for shipping working software:

  1. Decide to work on something by checking
    [Pivotal Tracker](http://scottchacon.com/2011/08/31/github-flow.html)
    or a new idea you think would be awesome (put it into the tracker)
  2. Branch off master

     ```bash
     $ git checkout -b myfeature master
     ```
  3. Work
     * Regularly commit and push to the server

       ```bash
       $ git push origin myfeature
       ```
     * If you're not sure about a small chunk of code, create a
       [gist](https://gist.github.com/) then post it in campfire / google group.
       Or just open a Pull Request.
  4. Open a Pull Request\*\*
  5. Merge with master after review and delete branch if it is done

     If working locally, merge with a no fast forward when possible:

     ```bash
     $ git checkout master
     Switched to branch 'master'
     $ git merge --no-ff myfeature
     Updating ea1b82a..05e9557
     (Summary of changes)
     $ git branch -d myfeature
     Deleted branch myfeature (was 05e9557).
     $ git push origin master
     ```
  6. Wait for Travis to report all tests pass
  7. Deploy immediately

>_\*\* "Pull requests are dicussions, that improve
>code quality" - Zach Holman [How Github Works](http://zachholman.com/posts/how-github-works/)_

>_While this frees up time from micromanaging, we are still learning,
  and want to learn together. So we will have code reviews (for now)
  before merging. The review process is simple:_

>  * _Once you want something to go back into master submit a pull
      request_
>  * _Email notifications will be sent, and messages added to campfire. As soon
      as a majority of people sign off on it (fun time to use
      [Emoji](https://gist.github.com/981817) you can merge_
>  * _If there is something more, group feedback will be provided to
      help guide you; or we can submit it for a group pair session the
      following week_

