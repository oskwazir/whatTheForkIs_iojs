# What the fork is io.js?

A presentation for the TucsonJS Meetup.

Notes

## First there was node.js
node.js was created in 2009 by Ryan Dahl
gave us JavaScript everywhere ~ robots ~ servers ~ tooling
open source and led by Benevolent Dictator for Life
Sponsored by Joyent

##node intentionally moving slowly
fell behind V8 and libuv supported versions

##features not rolling in fast enough

##node.js responds 
2015.02.06, Version 0.12.0 
* npm: Upgrade to 2.5.1
* mdb_v8: update for v0.12 

##libuv
"libuv turns out to be a rather useful library itself: a BSD-licensed, minimal, high-performance, cross-platform networking library.":http://blog.nodejs.org/2011/09/23/libuv-status-report/


##V8
chrome stable 4.2.77.14
`node -e 'console.log(process.versions.v8);'`
http://omahaproxy.appspot.com/
Stable:4.2.77.14
iojs-1.8.1: 4.1.0.27
nodejs-v0.12.2: 3.28.73
nodejs-v0.10.38: 3.14.5.9

#libuv
nodejs-v0.12.2: 1.4.2-node1
nodejs-v0.10.38: 0.10.36
iojs-1.8.1: 1.4.2

##io.js what you need to know
https://gist.github.com/maxogden/d96123138522c84cdb25
ECMA
open source competition
applying competitive pressure

##corporate ownership of open source

Mikeal Rogers [On Corporate Ownership of Open Source](https://medium.com/@mikeal/on-corporate-ownership-of-open-source-786ebd15847e)
> can *__any__* company be trusted with the ownership of a community driven open source project? And the answer I’ve finally come to. *No*.

##reconciliation
3-6 months based on Node.js Foundation Development Policy Call (2015-04-13) 
Diffing io.js and the Node.js Foundation https://github.com/iojs/io.js/issues/1416

##LTS


So are io.js and Node.js going to merge?
That has not been decided. What we're trying to do here is figure out what that would actually look like and push it in a direction that is acceptable to everyone.

I'm not convinced of the necessity of having a board
A board is a legal requirement for having a non-profit.

that the TC does not want to be responsible and lead and build the tools to automate the decision and management processes

This isn't a technical problem. If it were then LegalZoom would have a way for us to setup and manage the non-profit. Non-profit accounting and administration is somewhat specialized and the information not entirely accessible to everyone. This comes up whenever someone says "just start a foundation." It's not that simple, it's the opposite of simple, because the government really doesn't want people starting them.

By comparison getting a company and handling the accounting is quite easy and straightforward, I have an LLC that I use to run the conferences under and it's a fair amount of work but was something I could figure out and find a lot of relevant documentation on. I clicked some buttons on LegalZoom and had a license in a few hours and a bank account a week later. That's because the government wants people to start businesses. Unfortunately having a for-profit entity owning project assets is what got us in this mess in the first place so this isn't an option.