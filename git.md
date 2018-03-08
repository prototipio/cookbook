### Commit message

If you commit simple typo fix or rename something, please use shorthand for commit message:*

$ git commit -m 'Fix typo in rails_helper'

And commit will look like this one:

commit 797f8beea2c63e9e91c7c2bf90edc4d588704f60
Merge: 174c666 a523113
Author: Name <name.surname@company.email>
Date:   Sun Mar 4 00:25:44 2018 +0200

    Fix typo in rails_helper
    
If you submit more valuable changes, please use full text message 

$ git commit

# => Write some text description like below:

Add Capybara driver option for system tests

System tests use a method called driven_by, which is part of Rails core,
and which manages the Capybara driver configuration. The argument to driven_by
is the Capybara driver. The default is :selenium, but you can also use
:rack_test, :selenium_chrome, or :selenium_chrome_headless.

I have added :rack_test as using by default to run all system tests
(except one which using javascript or :js tag).
For example to run system tests in interactive mode, just
pass the ENV varible before calling RSpec:

DRIVEN_BY=selenium rspec spec/system

And commit will look like this one:

commit cb9592396ed7697b044cd3dd261afca67f889051
Author: Name <name.surname@company.email>
Date:   Tue Mar 6 09:17:49 2018 +0200

    Add option to choose driver to run RSpec system tests
    
    System tests use a method called driven_by, which is part of Rails core,
    and which manages the Capybara driver configuration. The argument to driven_by
    is the Capybara driver. The default is :selenium, but you can also use
    :rack_test, :selenium_chrome, or :selenium_chrome_headless.
    
    I have added :rack_test as using by default to run all system tests
    (except one which using javascript or :js tag).
    For example to run system tests in interactive mode, just
    pass the ENV varible before calling RSpec:
    
    DRIVEN_BY=selenium rspec spec/system
    
    *Base article https://chris.beams.io/posts/git-commit/
