Turtle XP Tracker  v1.1
=======================

A stable XP/hour tracker for Turtle WoW with a proper Vanilla UI.

Why this one doesn't "randomly reset"
-------------------------------------
  - XP/hour = TOTAL session XP / TOTAL active seconds. It never drops a
    window of old data, so the number stabilizes the longer you grind.
  - Session data is saved per character. Logging out, /reload, and
    zoning will NOT wipe your session. Only /xp reset does.
  - Time only counts while you're logged in, so being offline does not
    deflate your rate.

What you see
------------
  XP/hr        Cumulative session average (the stable number)
  Session      Total XP gained and active time this session
  Level X      Current XP / XP needed + percent
  To level     Estimated time-to-ding at the current XP/hr
  Kills        XP-awarding kills + average XP per kill
  Rested       Rested XP pool + % of the level it covers
  XP bar       Purple bar with a blue "rested" overlay — same colors
               as the Blizzard default XP bar.

Installation
------------
Files already live in:
    WoW\Interface\AddOns\TurtleXPTracker\

1. Fully quit WoW (needed only on first install, so the client picks
   up the new folder).
2. At character select, click "AddOns" bottom-left and make sure
   "Turtle XP Tracker" is enabled.
3. Log in. The frame appears above your character.

Moving & resizing
-----------------
  - DRAG anywhere on the frame to move it.
  - DRAG the small grip in the bottom-right corner to resize.
  - SCROLL WHEEL over the frame to change text size (8-24).
  - /xp lock       Freeze the frame so you can't move or resize it.
  - /xp unlock     Allow moving/resizing again.

Slash commands
--------------
  /xp                 Toggle the window
  /xp reset           Reset session XP, time, kills
  /xp reset pos       Reset just the window position
  /xp reset all       Reset everything (settings + session) to defaults
  /xp show            Show the window
  /xp hide            Hide the window
  /xp lock            Prevent dragging / resizing
  /xp unlock          Allow dragging / resizing
  /xp font <6-32>     Set text size (same as scroll-wheel)
  /xp scale <0.5-2>   Set overall UI scale (makes the WHOLE addon
                      bigger or smaller, icons and all)
  /xp size WxH        Set exact window size, e.g. /xp size 320x180
  /xp help            Print all commands

Font size vs. scale vs. size — what's the difference?
-----------------------------------------------------
  - font   -> only changes the text size inside the frame
  - scale  -> multiplies the whole addon (frame, text, bar) uniformly
  - size   -> width and height of the frame in pixels (text doesn't
              change)
Use "scale" if you just want bigger/smaller overall.
Use "font" + "size" together if you want tight control over the layout
(e.g., a wide frame with small text for a single-row look).

Tips
----
  - Always start a grind with /xp reset so the number reflects only
    this session of this activity.
  - The XP/hr figure will swing around for the first few minutes and
    then converge. That's the intended behavior — a 4-hour average is
    more useful for comparing farm spots than a jumpy 5-minute window.
  - Rested XP in Vanilla doubles mob XP until the rested pool is spent.
    Watch the blue rested bar shrink as you grind.
