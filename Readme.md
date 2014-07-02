*Disclaimer: This post is a work in progress. I wanted to release a [minimum viable](https://www.youtube.com/watch?v=_a3s0IXSuxY) version of this post to solicit input. Hopefully you will help me make this better. :-) To do so, tweet @datascimed, leave a comment below, or [fork this post](https://github.com/cb01/sciworkflow) on GitHub.*

*This is the development version of the post. View the most current release at [datascimed.ghost.io]{http://datascimed.ghost.io/naupakas-mac-sci-coding-stack/}*

--

I'm at the [Stanford Software Carpentry (SWC) bootcamp](http://ivanov.github.io/2014-06-30-stanford/) today and got some great suggestions from one of the SWC intstructors Naupaka Zimmerman ([@naupakaz](https://twitter.com/naupakaz); [naupaka.net](http://naupaka.net)) on apps for the Mac to enhance productivity for academics developing software and analyzing data.

#### Terminal and text

According to Naupaka, "The first thing you should do is download and install [iTerm](http://iterm.sourceforge.net/)", an alternative to Apple's terminal app. Also key is having the right text editor. For those who prefer a GUI, [Sublime Text](http://www.sublimetext.com/) is a top choice. It has a rich collection of [plugins](https://sublime.wbond.net/) to extend its default feature set. In addition, Sublime provides shortcuts to check and run code. To save even more time, snippets of text you use repeatedly or would like to have templated can be stored and injected using [Text Expander](http://smilesoftware.com/TextExpander/index.html). When you're using R in a graphical environment, he also suggests [RStudio](http://www.rstudio.com/) which has built-in capability for interacting with git-versioned repositories.

Despite all the GUI text editors available, Naupaka prefers [vim](http://www.openvim.com/tutorial.html) for his development - either directly in the shell (zsh with [oh-my-zsh](http://ohmyz.sh)) or via [MacVim](https://code.google.com/p/macvim/). Vim is available by default on all -nix distributions. This means any server you log into will have this available by default. Those who have been developing for a long time may have their own highly customized vim environment, including customizations to automatically check python code for syntax errors, to display the current git branch, line numbers, and more. Furthermore, coloring can be customized in vim (Naupaka likes the "Twilight" scheme from [TextMate](http://macromates.com/) but also pointed out the [Solarized color scheme](http://ethanschoonover.com/solarized)). Any good text editor will offer language-specific syntax coloring (which vim supports; many others here). Lastly, if you log into a new machine you will probably want all of your extensive customizations available on that machine. In order to do so, Naupaka suggests pushing your vim configuration file to GitHub and cloning that to the new machine when you log in.

#### Version control

Recently, [git](http://git-scm.com/) has become the dominant version control system. Naupaka uses [Tower](http://www.git-tower.com/), a graphical git client, but also mentioned [SourceTree](http://www.sourcetreeapp.com), which is free. For complicated merges, he uses [Kaleidoscope](http://www.kaleidoscopeapp.com/) to view diffs graphically (plus it does three-way merging!), which can be set as the default diff viewer for both Tower and the command-line Git utility. Interestingly, is also capable of visualizing diffs on folders.

#### Digital workspace

Keeping your windows, files, and apps under control is also key. Naupaka uses [Moom](http://manytricks.com/moom/) for managing the sizing and position of windows. He has set shortcuts that allow windows to be placed in chosen segments of the screen, saving time on clicking and dragging their corners to exactly the right size. It can simplify things to have only three windows open, a text editor (1/4 screen), an iTerm terminal (1/4 screen), and a web browser (1/2 screen).

On the Mac, Spotlight is great but Naupaka prefers [Launchbar](http://www.obdev.at/products/launchbar/index.html), [Alfred](http://www.alfredapp.com/), or [Quicksilver](http://qsapp.com/). There is also a path browser alternative to Finder available, [Path finder](http://cocoatech.com/pathfinder/).

#### Backup

If your drives containing all of your code and writing for your dissertation fail, you will haz problem. That's why it is worth your time to design and implement a thorough data backup and redundancy plan. Naupaka suggests using [Dropbox](http://dropbox.com) as your first tier of backup, which can be used both to sync files present in the normal Dropbox folder as well as files and folders with symbolic links within that folder (link to blog post). For the next tier, he recommends having your files backed up locally, such as to an external drive. It is often useful to have both the versions supported by Time Machine AND a full clone of the drive. For full drive, bootable backups he likes [Super Duper](http://www.shirt-pocket.com/SuperDuper/superduperdescription.html) and [Carbon Copy Cloner](http://www.bombich.com/). The deepest level of backup he recommends is saving your files to [Amazon Glacier](http://aws.amazon.com/glacier/), facilitated by the program [Arq](http://www.haystacksoftware.com/arq/). Glacier [pricing](http://aws.amazon.com/glacier/pricing/) is $10/TB per month with free transfer in and around $0.12/GB for transfers out (if you ever need to retrieve your backups from the deep freeze). 

In addition to your backup, [1Password](https://agilebits.com/onepassword) makes password management convenient (never reuse a password more than once!).

#### Project management

Significant time can be wasted in software development projects that were not conducted according to a thorough plan. That's why it's good to start any project with whiteboard markers and lots of input. Once you have a plan, it's valuable to diagram the dependencies of your functions and modules. If your project involves anything but a trivial amount of data, starting with a clear data management plan is good as well. If you're using databases, that means planning their structure ahead of time. 

Once you're ready to translate the structure of your project into a development plan, Naupaka suggests [OmniPlan](http://www.omnigroup.com/omniplan), and noted [Merlin](http://www.projectwizards.net/en/merlin/) as another good option. Here you can list the major tasks of the project, indicate their dependencies, and assign them to individual developers in your project. For managing your own tasks (and general life organization), [OmniFocus](https://www.omnigroup.com/omnifocus) is a revolution. This allows you to manage individual todo items in a hierarchy of multiple projects and categories. Naupaka demonstrated some of the AppleScripts for OmniFocus that he uses (supports in the pro version of OmniFocus). 

#### Literature management

I'm interested in learning more about how to manage the onslaught of the scientific literature. Naupaka recommended [Reeder](http://reederapp.com/) for aggregation and filtering on the mac, and [Mr. Reeder](http://www.curioustimes.de/mrreader/) for the iPad. He uses [IFTTT](https://ifttt.com/) to automatically add tasks to OmniFocus every time he stars an RSS article in Reeder or a tweet on Twitter, allowing him to keep track of the materials he needs to read later. Some people also use IFTTT to send links to [Pinboard](https://pinboard.in) for this purpose.  He manages his bibliographies with [Bookends](http://www.sonnysoftware.com/). When I asked him what the advantages of that are over something like [Mendeley](http://www.mendeley.com/) (which I use/d), he emphasized the importance of the full-text search feature in Bookends. Other good alternatives are [ReadCube](http://www.readcube.com), [Papers2](http://www.papersapp.com) (sadly not Papers3), [BibDesk](http://bibdesk.sourceforge.net), [Zotero](https://www.zotero.org), and [Sente](http://www.thirdstreetsoftware.com/site/SenteForMac.html).

#### Digital lab notebook

I have experimented with keeping a digital lab notebook using [Evernote](https://evernote.com/) but the problem I ran into was that sync conflicts arose when I created a note on my desktop (e.g. a long laboratory protocol) and edited it on my phone (in the lab). Naupaka solves this problem by using Evernote with very high granularity (one note per gel image, microscope image, observation, etc.). Each of these can be tagged and are time stamped. Many notes can be organized into sets that take the place of the one-single-long-note-per-protocol approach I was taking. Icing the cake, Evernote provides image to text functionality which means that when you add photographs of your paper lab notebook to Evernote their text will be searchable.

#### Communication

Continuing this long list of amazing apps I had never heard of, Naupaka suggested [Mail mate](http://freron.com/), which allows you to write emails in Markdown and integrates with OmniFocus. For a Twitter client, he recommended [Tweetbot](http://tapbots.com/software/tweetbot/) for OS X and iOS, which saves your current reading position across devices and has lots of customizability. [TweetDeck](https://about.twitter.com/products/tweetdeck) is a powerful alternative that runs within the [Chrome](https://www.google.com/intl/en-US/chrome/browser/) browser. Sharing links on Twitter with [Droplr](https://droplr.com/hello) or [Bit.ly](https://bitly.com/) allows you to track clicks on those links. Droplr also allows you to share files with extreme ease (see also [CloudApp](http://www.getcloudapp.com/)), whereas Bit.ly is only for links. Naupaka also told me about some of his elaborate IFTTT connections for Droplr which I need more time to wrap my head around.

#### Collaborative manuscripts

We've been using [Authorea](https://www.authorea.com/) in the Eisen Lab for collaborative manuscript-ing and I'm interested in how to do this better. The dream here is to simultaneously have a simple interface (acceptable to Word users, i.e. P.I.'s) on top of the power of git and iPython. Naupaka noted that Authorea has the ability to be [linked to a git repository](https://www.authorea.com/issues/8) as well as to [work with iPython](https://authorea.com/users/3/articles/3904/_show_article). Paul Ivanov (another instructor at the SWC bootcamp today who did a fantastic job; [@ivanov](http://twitter.com/ivanov);  [http://pirsquared.org/](http://pirsquared.org/)), one of the iPython core developers, said [Google Docs integration](https://plus.google.com/app/basic/stream/z133vvygwpzxc3co404cchobnq3wzl25jik) is planned for iPython.

#### Work environment

Let's talk about your non-digital work environment. Naupaka's suggestion? "Don't get carpel tunnel. You need your fingers to do science." He suggested doing an audit of the positioning of your keyboard to remove pressure from your wrists. We also discussed [f.lux](https://justgetflux.com/), which is an app for automatically tinting your computer screen toward red in the evening to make it easier to fall asleep when you finish your 18h day of programming. I have one key suggestion and if you know me you've heard it: bike desk. Get your legs moving while you work ([Cheap stationary bike](http://www.amazon.com/Sunny-Health-Fitness-Indoor-Cycling/dp/B002CVU2HG) + [table from Ikea](http://www.ikea.com/us/en/catalog/products/90087541/)) and your brain will appreciate it.


#### Package management

In closing, Naupaka said "Make sure people know about [Homebrew](http://brew.sh/)", which allows you to install software and the multitude of their dependencies with simple commands like `brew install <complicated_program>`. He does not recommend using [MacPorts](http://www.macports.org/) or [Fink](http://www.finkproject.org/). For Python, both [conda](http://www.continuum.io/blog/conda) and [pip](https://pypi.python.org/pypi/pip) are great. I'll have a separate post all about development in Python.

#### The end

These are a lot of suggestions to digest. I'm hoping to also collect suggestions for Windows and Linux users but to keep these separate from the Mac suggestions. I would also like it if there was a way to make these suggestions more scientific, e.g. having people vote on their preferences, perhaps taking a page from Reddit. For now I'm looking forward to experimenting with each and sharing my perspectives. I hope you will also share yours, including alternatives to those discussed above. Tweet @datascimed or leave a comment below. Here's a summary of what we covered.

*Terminal and text*

* [iTerm](http://iterm.sourceforge.net/)
* [vim](http://www.openvim.com/tutorial.html)
* [Sublime Text](http://www.sublimetext.com/)
* [Text Expander](http://smilesoftware.com/TextExpander/index.html)
* [RStudio](http://www.rstudio.com/)
* [Solarized color scheme](http://ethanschoonover.com/solarized )

*Version control*

* [Tower](http://www.git-tower.com/)
* [Sourcetree](http://www.sourcetreeapp.com/)
* [Kaleidoscope](http://www.kaleidoscopeapp.com/)

*Digital workspace*

* [Moom](http://manytricks.com/moom/)
* [Launchbar](http://www.obdev.at/products/launchbar/index.html)
* [Alfred](http://www.alfredapp.com/)
* [Quicksilver](http://qsapp.com/)
* [Path finder](http://cocoatech.com/pathfinder/)

*Backup*

* [Dropbox](http://dropbox.com)
* [Super Duper](http://www.shirt-pocket.com/SuperDuper/superduperdescription.html)
* [Carbon Copy Cloner](http://www.bombich.com/)
* [Amazon Glacier](http://aws.amazon.com/glacier/)
* [Arq](http://www.haystacksoftware.com/arq/)
* [1Password](https://agilebits.com/onepassword)

*Project management*

* [OmniPlan](http://www.omnigroup.com/omniplan)
* [OmniFocus](https://www.omnigroup.com/omnifocus)

*Literature management*

* [Reeder](http://reederapp.com/)
* [Bookends](http://www.sonnysoftware.com/)
* [Mendeley](http://www.mendeley.com/)

*Digital lab notebook*

* [Evernote](https://evernote.com/)

*Communication*

* [Mail mate](http://freron.com/)
* [TweetDeck](https://about.twitter.com/products/tweetdeck)
* [Tweetbot](http://tapbots.com/software/tweetbot/)
* [Droplr](https://droplr.com/hello)
* [CloudApp](http://www.getcloudapp.com/)
* [Bitly](https://bitly.com/) 

*Work environment*

* [f.lux](https://justgetflux.com/)
* [Stationary bike](http://www.amazon.com/Sunny-Health-Fitness-Indoor-Cycling/dp/B002CVU2HG)
* [Ikea table](http://www.ikea.com/us/en/catalog/products/90087541/)



