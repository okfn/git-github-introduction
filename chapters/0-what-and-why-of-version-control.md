The What and Why of Version Control
===================================

Many people know this situation, you are working on a document, change
something and are less happy with what you changed then what was there
before. How do you undo it? This is where version control comes in.

Simple version control is just to save files for each revision you make
(e.g. start out with a document, then copy it to a new version number, edit
that one and so on). This is how the first version control systems worked.
More advanced version control systems actually don't store the whole file
anymore - they only store the changes you made. 

Version control becomes especially valuable when working with multiple
people - imagine you are writing a text with your friend and you both edit.
This is a common problem. Therefore programmers started working on version
control systems that had servers, where everyone working on a document
could write their changes to - so documents are updated automatically for
all of them. So if we don't edit the same line, the version control system
can figure out how to merge edits together. 

The first version control systems were dependent on a single server and not
very good at mergin different changes together. Git fixes both these
things: it is a decentralized version control system that is very good at
figuring out how changes are supposed to be merged together.

Decentralized version control simply means that each copy of the repository
- a repository is simply a folder managed with git - is equivalent to each
other copy and could serve as a reference for future projects. Sounds
complicated? It's not so much.

Imagine Alice and Bob work on a text together, Alice starts and decides to
use git. She makes sure all her changes and documents are in there and
publishes a repository. Now Bob can take her repository do some changes and
publish his own repository. Alice is now free to get the changes Bob made
from Bob and merge them with her version. 

Now if Claire a friend of Bob wants to contribute, she copys Bobs
repository and works on it. She alerts Bob and Alice of the changes, now
Alice can decide to take Claires changes as well. If not, Bob can still
take the changes and have a slightly different version from Alice (however
all the changes can still be merged back if needed).

So let's get our hands dirty...

