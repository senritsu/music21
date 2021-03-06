.. _usersGuide_01_installing:
User's Guide, Chapter 1: Installing and Getting Started with ``music21``
========================================================================

If you're going to use ``music21``, you'll need to have a copy of it and
Python on your computer. The instructions are slightly different for
each type of computer, so follow the link below and then come back to
the system. For many people, installation is the most difficult step for
a bit.

Mac users: :ref:`installMac`

Windows user (also installs Python): :ref:`installWindows`

Unix/Linux users or advanced Mac users: :ref:`installLinux`

Advanced users who are familiar with Python installations can read
:ref:`installAdvanced`.

When a new version of ``music21`` is released, you can upgrade by using
the same method that you originally used to install it.

If you want to see if it's worth installing, keep
:ref:`reading the guide <usersGuide_02_notes>` without installing, but
if you have installed already, you'll get more out of the guide since
you'll be able to follow along.

Starting ``music21``
--------------------

We'll just see if music21 worked for you. Open up the Terminal (Mac) or
IDLE (Windows). On the Mac type "python" (without the quotes) and hit
enter.

To load music21 type this, always omitting the ">>> " below:

::

    >>> from music21 import *

You'll probably get a few warnings that you're missing some optional
modules. That's okay. If you get a warning that "no module named
music21" then something probably went wrong above. Try going
step-by-step through the instructions above one more time, making sure
not to skip anything. 99% of installation errors come from skipping a
step above. If you still have a problem, Google for "installation
problem music21" or "installation problem mac python module" and see if
anything looks familiar. If all else fails, contact the music21list
Google Group which might be able to help.

If you didn't have a problem, which is nearly always the case, then
music21 has worked for you. Test that you can get a score from the
corpus by typing this command:

::

    >>> s = corpus.parse('bach/bwv65.2.xml')

Now ``s`` represents an entire score of a chorale by J.S. Bach. Type
"``s.analyze('key')``\ " to see what music21's best guess as to its key
is. There's lots more that you can do as we'll see later. But there's
one more thing to test. Let's see if you can get music notation
(assuming you installed a MusicXML reader above).

Type "``s.show()``\ " or if you want to be more precise,
"``s.show('musicxml')``\ "

Assuming your installation and configuration went as expected, your
MusicXML reader should launch and display the chorale, looking something
like what we see here:

.. image:: images/macScreenShow.*
    :width: 650

If you don't have ``MusicXML`` working for you yet, don't panic, we'll
give more explicit instructions in a few chapters. For now, let's
proceed to :ref:`usersGuide_02_notes`.
