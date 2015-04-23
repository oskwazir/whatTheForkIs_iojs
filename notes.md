#What the fork is io.js

##Introduction
My name is Omer Wazir, sounds like Boomer without a B. oomer. I work as a software engineer for Tucson Embedded Systems. Today I will talk about io.js, I'll explain why it was created and why it matters. This won't be a very techincal discussion. I won't be explaining API's or showing any code. Just want to help you understand what io.js is and how it relates to node.js

##first there was node.js
It's going to be difficult to talk about io.js without explaining a little bit of the history of node.js. node.js was created in 2009 by Ryan Dahl. Ryan
wanted to create a purely evented, non blocking infrastructure to write highly concurrent programs, because synchronous I/O doesn't really make sense for server apps. He explains node.js by giving an example of a web server querying a database synchronously and the web server just waits until the response comes back. A lot of CPU time is wasted during this waiting period. Using threads instead is difficult because of blocking. It's easier to just have one thread. You don't block and just write a callback to handle responses. JavaScript was already geared towards events and callbacks and it didn't have an existing API for I/O. node.js depends on Google's V8 engine for executing JavaScript.

Eventually Ryan got a job at Joyent, transferred ownership of the trademark and copyright of node.js to Joyent. Ryan no longer works on node.js. Today node.js is open source under an MIT license but it's governed by Joyent and led by a benevolent dictator.

##node.js was progressing slowly
The node ecosystem has about 140,000 packages available, with 1.2 billion downloads in the last month. Yet the development on node.js itself had dropped and releases had slowed down. So a lot of people are active in the node ecosystem but contributions to node core and releases decreased. I'm not really sure why this downturn happened. Why were people not contributing to node.js, and why were releases taking so long? Joyent should have fixed this since they own and guide the project. Core contributors wanted to take over the project to fix this problem since it didn't seem like Joyent was making any progress.

##node forward started
http://www.infoworld.com/article/2855057/application-development/why-iojs-decided-to-fork-nodejs.html
So there's momentum building up towards addressing the problems with node.js. Node Forward was created as a way to discuss and solve the problems with node.js. As I understand node.js was forked but because of trademark issues the repo where Node Forward was doing work had to be made private. Node Forward thought "the best way to move Node forward is to get the community organized around solving problems and putting out releases". If you read through the discussions that happened at the Node Forward site you'll see a lot of stuff that lead to io.js. 

##private node.js fork turned into io.js
Fedor Indutny who was a node.js contributor and he got tired of making private patches to the forked node.js repo, and just made it public under the name of io.js. All of the work done at Node Forward moved to io.js. io.js operates under a open governance model. There's a technical committee of contributors which takes contentious issues to a vote. Majority wins. As far as I can tell all discussions happen openly on the io.js org github site.  TC meetings are open to listen to and saved on YouTube and SoundCloud.

##the technical committee
TC has final authority over io.js including
  Technical direction
  Project governance and process (including this policy)
  Contribution policy
  GitHub repository hosting
  Conduct guidelines
  Maintaining the list of additional Collaborators

 Meetings are open to the public to listen to. Issues can be discussed on the io.js org github site.

##core team behind io.js
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
works with npm
because the path to the node binary is a major dependency, iojs redirects that path to it's own path
I prefer to use nvm to manage io.js and node.js installs


##does node.js v0.12 close the gap?
nope. the difference between io.js and node.js is not just technical features, there is the governance model, the contribution policy and the quicker
release cycle.


##io.js has gained a lot of momentum
Whatever io.js did differently from node.js, it seems to have worked. The graph doesn't show contributions from merged forks, just commits from 
core members. There is also a lot of work behind managing issues and handling discussions. I don't know of a good way to display any of that but I think
we know it's working because node.js is interesed in merging with io.js.

##reconciliation
io.js offered a proposal to node.js to merge the projects together. io.js was always open to returning to node.js it was just a matter of Joyent and
other the io.js TC accepting reconciliation. the proposal io.js offered was to adopt the Governance, Contributing, Working Groups and Roadmap structure.
the contributors from io.js would remain and six collaborators from node.js would be adopted (3 on the TC).

LTS is also being planned.

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