Dealing with Legacy Code
Engine Upgrades
at 35,000 feet

On a completely full passenger jet

[airplane pic]


1. What is legacy code
    1. Include based
    2. php 3 / 4 style
    3. Mixed of html and php
2. What are we trying to accomplish?
    1. Testability
    2. Flexibility (easier to change)
    3. Continuity
3. What to avoid
    1. Grand Rewrite
    3. Making multiple changes across files
    4. Shoe-horning a framework
    2. Over-engineering
3. First steps
    1. Git
    2. autoloader (composer)
        1. Location for classes
    3. Automated Deploy
    4. Config loader by environment `return (getenv(self::APP_ENV)) ?: 'local';`
    5. A Symfony2 Request
    6. A Template system
4. Testing
    1. Testing Framework
        1. Mink (http://mink.behat.org/)
        2. CasperJS
    2. QA environment
        1. Database snapshot
        2. Available to principles
        3. As close as possible to production
5. How to approach the codebase
    1. Choose a page
    2. Write tests for the page
    3. Do one thing
    4. Confirm tests
    5. Commit often!
6. One Things to do
    1. Replace function includes with autoloading
        1. Choose 1 include
        2. Choose a classname
        3. Copy a file in class location
        4. Replace all functions with static methods - do not change them!
        5. Repeat
    2. Includes with both functions and logic (sideffects) - put logic in init method - by reference
    3. Move all logic code above template
    4. Move all database queries out to repositories
    5. Move to controller, change superglobals to use Request
6. Adding new features
    1. Use your new tools
    2. Build just the things you need
    3. Improve anything that interacts (Boy scout rule)
    4. It can be done!
7. How do I know when I'm done?
    1. This is just the beginning
    2. Extract domain logic
    3. Front controller










