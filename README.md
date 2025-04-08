# Spelunky 2 FMOD Template Project

This project was built with FMOD Studio version 2.02.17.
Spelunky 2 uses FMOD Studio version 2.02.03, however
FMOD Studio projects are both backwards and forwards
compatible as long as they are within the major version
(2.02.xx).

## FMOD Projects

**spelunky2-mods** is a blank FMOD Studio project containing
nothing besides the necessary buses required to route audio
into Spelunky 2's mixer.

**spelunky2-bgm-master-template** is an FMOD Studio project
which currently contains a single event. This event is a
best-guess attempt to recreate the functionality of
Spelunky 2's BGM_master event. It contains multiple
pre-defined parameter sheets, audio tracks and empty
event instruments that have been routed to the
correct returns, along with automation curves for
the ghost parameter. It also contains identical
parameters to Spelunky 2's BGM_master. The mixing
will sound strange since the sends for each audio
track have not been extensively tweaked.

## Avoiding GUID Collisions

If you decide to use the **spelunky2-bgm-master-template**,
open the **spelunky2-mods** project along with it. Right
click the BGM_master event and select Copy. Paste it into
the **spelunky2-mods** window using Edit > Paste. FMOD will
copy the event to the other project, and more importantly
assign it a new GUID. This is to ensure that your event has
a unique GUID, and that GUID collisions do not occur if
playing with multiple mods that use the BGM_master template.