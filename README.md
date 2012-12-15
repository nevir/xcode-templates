Better Xcode Templates
======================

Let's face it, Xcode's bundled templates are less than ideal.  You've got a
mixed code styles, not-so-best practices, annoyances, and plenty more.

It's pretty easy to use:

    git clone https://github.com/nevir/xcode-templates
    xcode-templates/install

At the moment, this is focused entirely on project templates; [file templates
might be a while out](#rough-edges).

So, what do you get?
![Project Template Configuration](http://nevir.github.com/xcode-templates/images/configuration.png)


Your Favorite Code Style
------------------------

Indeeder!

* You can have your `{` on a new line if it pleases you.

* You no longer need to answer the age old quandry of whether the `*` part of
  the type, or the variable.

* Maybe you like variable names all scrunched up with their types in
method signatures; maybe you don't.

* Perhaps you find file headers redundant.  You can even turn them off!

What is _wrong_ with this world?!


Modern Objective-C Only!
------------------------

These templates drop compatibility for a more modern feeling:

* You're using ARC and you are going to like it that way.

* `[foo bar]` bad.  `foo.bar` good.

* Objective-C object literals are liberally applied.


Configuration via xcconfig
--------------------------

Having a configuration format that is not a GUI-managed XML mess (your project
file) can be liberating.  Don't say I didn't warn you when you're running
through the streets with an iguana on your head proclaiming the joys of being
able to sanely review your collaborators' cofiguration changes.


Storyboards
-----------

Yeah, I know, change is bad.  However, storyboards also happen to be nibs/xibs,
with _even more benefits_ and _fewer downsides_; stop resisting them!

Anyway, nothing's stopping you from using nibs/xibs for one-off controllers if
you really feel the need.


Autoresizing
------------

Constraints are great for simple layouts, but Xcode's wonky behaviors make them
a pain to work within in storyboards/nibs/xibs.  They'll get there one day, but
for now, your life is probably a lot safer and saner using autoresizing masks.


Icons & Splash Screens
----------------------

They're there to make you look good.  Also, there are a crazy amount of icons
that you should be filling in; it's good to have a template.

You're welcome to (ab)use the image assets in your projects if you like; pub
domain.


More Project Structure
----------------------

Xcode projects tend to defy reality by aggressively grouping files while
splatting everything into a handful of folders on disk.  A strong tenet of
these project templates is that groups match the file system!

Also, there are probably more groups than you're used to.  Maybe you won't have
to shuffle everything around after generating a project, eh?


Template Organization
=====================

When reasonable, these templates attempt to mirror the structure of Xcode's
bundled templates.  There are a few organizational rules to hopefully make
finding things a bit easier:

* Templates identifiers mirror their file path and name.  For example,
  `iOS/Common/Cocoa Application` has an identifier of
  `net.nevir.xcode-templates.ios.common.cocoa-application`.

* Any macros, definitions, or options relating to code style are contained in
  the code style templates under [`Common`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common).


Rough Edges
===========

Unfortunately, as best I can tell, there are some limitations that cannot be
overcome w/ the current (vanilla) Xcode:

* [The configuration you specify at the project level cannot be carried across
  to file templates](http://stackoverflow.com/questions/13042974).

* [It doesn't look like we can get a xcconfig per target](https://github.com/nevir/xcode-templates/blob/4432e75fb9bdd0ac48d7dfcbdd025334e03d72dd/Project%20Templates/Common/Base.xctemplate/Templateinfo.plist#L102)

* [Not all settings can be set via the xcconfigs](https://github.com/nevir/xcode-templates/blob/4432e75fb9bdd0ac48d7dfcbdd025334e03d72dd/Project%20Templates/iOS/Common/Base.xctemplate/Templateinfo.plist#L22)


License
=======

_Don't be a dick._

Here's some suggestions:

* Give attribution if you package this project.

* Contribute back!  Better Xcode templates are a boon to mankind!

Also, this project contains resources from Apple's official Xcode templates; I
make no claim to them, and you shouldn't either.
