#What the fork is io.js

##Introduction
My name is Omer Wazir, sounds like Boomer without a B. I work as a software engineer for Tucson Embedded Systems. I write a lot of JavaScript but I don't support node in production. Which means I get to have all the fun I want writing node without caring what the customer sees. Today I want to talk about io.js to you, I'll explain why it was created and why it matters. This won't be a very techincal discussion.
I won't be explaining API's or anything exciting like that. Just want to help you understand what io.js is and how it relates to node.js

##first there was node.js
It's going to be difficult to talk about io.js without explaining a little bit of the history of node.js. node.js was created in 2009 by Ryan Dahl. Ryan
wanted to create an purely evented, non blocking infrastructure to write highly concurrent programs, because synchronous I/O is poor for server apps. He explains node.js by giving an example of a web server querying a database synchronously and the service just waits until the reponse comes back. A lot of time is wasted during this waiting period. Threads are difficult to work with because of blocking. It's easier to just have one thread. You don't block and just write a callback to handle responses. JavaScript is already geared towards events and callbacks and it didn't have an existing API for I/O.

Eventually Ryan needed some money so he got a job at Joyent, transferred ownership of the trademark and copyright of node.js to Joyent. node.js is open source under an MIT license but it's governed by Joyent and led by a benevolent dictator.

##node.js was progressing slowly
Although the node ecosystem has about 142,722 packages available, with 1.2 billion downloads in the last month the contributions to node.js have dropped. So a lot of people are using node.js but contributions to node core and releases started to slow down. I'm not really sure why this downturn happened. Whatever caused it the problem had to be addressed. Joyent should have fixed this since they own and guide the project. Core contributors wanted to take over the project to fix this problem since it didn't seem like Joyent was making any progress.

##node forward started
http://www.infoworld.com/article/2855057/application-development/why-iojs-decided-to-fork-nodejs.html
Node Forward was created as a way to address the problems with node.js. As I understand node.js was forked but because of trademark issues the repo where Node Forward was doing work had to be made private. Node Forward thought "the best way to move Node forward is to get the community organized around solving problems and putting out releases". If you read through the discussions that happened at the Node Forward site you'll see a lot of stuff that lead to io.js.

##private node.js fork turned into io.js
Fedor Indutny who was a node.js contributor and he got tired of making private patches to the forked node.js repo, and just made it public under the name of io.js. All of the work done at Node Forward moved to io.js. io.js operates under a consensus seeking model. There's a technical committee (7 people) of contributors which takes contentious issues to a vote. Majority wins.

TC has final authority over io.js including
  Technical direction
  Project governance and process (including this policy)
  Contribution policy
  GitHub repository hosting
  Conduct guidelines
  Maintaining the list of additional Collaborators

 Meetings are open to the public to listen to. Issues can be discussed on the io.js org github site.

##the community behind io.js
29 people, 7 on the TC. Pretty much all contributors on node.js who weren't working for Joyent work on io.js.
Some familiar names:
Isaac Z. Schlueter (npm)
Fedor Indutny
Rod Vagg (levelup)
Ben Noordhuis
Bert Belder
Trevor Norris

##io.js impact on  you
https://github.com/iojs/io.js/blob/master/ROADMAP.md
"Shipping with current and well supported dependencies is the best way to ensure long term stability of the platform. "
"Version 1.8.1 of io.js ships with V8 4.1.0.27, which includes ES6 features well beyond version 3.28.73 that ship with Node.js™ 0.12.x."

With io.js@1.x (V8 4.1+), all that complexity goes away. All harmony features are now logically split into three groups for shipping, staged and in progress features:

    All shipping features, the ones that V8 has considered stable, like generators, templates, new string methods and many others are turned on by default on io.js and do NOT require any kind of runtime flag.
    Then there are staged features which are almost-completed features that haven't been completely tested or updated to the latest spec yet and therefore are not considered stable by the V8 team (e.g. there might be some edge cases left to discover). This is probably the equivalent of the state of generators on 3.26. These are the "use at your own risk" type of features that now require a runtime flag: --es_staging (or its synonym, --harmony).
    Finally, all in progress features can be activated individually by their respective harmony flag (e.g. --harmony_arrow_functions), although this is highly discouraged unless for testing purposes.

Block scoping
  let
  const
  function-in-blocks
Collections
  Map
  WeakMap
  Set
  WeakSet
Generators
Promises
New String methods
Symbols
Template Strings


##io.js impact on your computer


##does node.js v0.12 close the gap?
nope.


##io.js has gained a lot of momentum

##reconciliation

##participation
Website
Streams
Build
Tracing
i18n
Evangelism
Roadmap
Docker


##questions?