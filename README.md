# Sixth Sense Tick Timer for World of Tanks

A lightweight World of Tanks Sixth Sense audio mod that plays an exact 12-second ticking sequence whenever Sixth Sense activates.

Designed as a simple situational-awareness timer without reading or exposing hidden gameplay information.

---

## Features

* Exact 12-second audio sequence
* Automatically starts when Sixth Sense activates
* Audible elapsed-time reference
* No external libraries
* No gameplay automation
* No hidden enemy or spotting-state detection
* Supports `.wotmod` and manual installation

---

## Installation

Two installation methods are available.

Use only one.

### Method 1: `.wotmod`

1. Close World of Tanks.
2. Open your World of Tanks installation directory.

Typical Steam installation:

```text
C:\Program Files (x86)\Steam\steamapps\common\World of Tanks\
```

3. Open:

```text
mods\<current_game_version>\
```

4. Copy the supplied `.wotmod` file into the folder.

Example:

```text
World of Tanks\
└── mods\
    └── <current_game_version>\
        └── SixthSenseTickTimer.wotmod
```

Do not extract the `.wotmod` file.

> After a World of Tanks update, you may need to move or reinstall the mod into the newly created version folder.

---

### Method 2: Manual Method

The manual method installs the Sixth Sense audio file directly.

1. Open:

```text
res_mods\<current_game_version>\
```

2. Create the following folder if it does not already exist:

```text
audioww
```

3. Copy the supplied audio file into:

```text
res_mods\<current_game_version>\audioww\
```

4. The audio file must be named:

```text
sixthSense.mp3
```

Final structure:

```text
World of Tanks\
└── res_mods\
    └── <current_game_version>\
        └── audioww\
            └── sixthSense.mp3
```

---

## Enable the Sound

Start World of Tanks and open:

```text
Settings
→ Sound
→ Sixth Sense Activation Sound
→ User sound
```

Select:

```text
User sound
```

The 12-second ticking sequence will now play whenever Sixth Sense activates.

---

## How the Timer Works

The timer starts the moment the normal Sixth Sense warning activates.

```text
Sixth Sense activates
        ↓
12-second ticking sequence begins
        ↓
Tick...
Tick...
Tick...
        ↓
12.0 seconds elapsed
        ↓
Sequence ends
```

The audio lasts exactly:

```text
12.0 seconds
```

Its purpose is to provide an audible indication of elapsed time while allowing you to keep your attention on the battle.

---

## What the Ticks Mean

The timer measures:

```text
TIME SINCE SIXTH SENSE ACTIVATED
```

It does not measure:

```text
TIME SINCE ENEMY VISION WAS BROKEN
```

Those are not necessarily the same thing.

### Example

If you immediately move behind hard cover after Sixth Sense activates:

```text
Sixth Sense activates
        ↓
You break enemy vision
        ↓
12-second timer continues
        ↓
Sequence ends
```

The timer can act as a useful reference for how much time has passed.

However, if you remain exposed:

```text
Sixth Sense activates
        ↓
You remain visible for 5 seconds
        ↓
You move behind cover
        ↓
7 seconds remain on the timer
```

The sound still ends exactly 12 seconds after Sixth Sense originally activated.

It does not restart when you break line of sight.

---

## Important

The end of the timer does not guarantee that your vehicle is unspotted.

Your actual spotting state may depend on:

* When enemy vision was broken
* Whether another enemy is still spotting you
* Whether you become visible again
* Crew perks or spotting-related game mechanics

Think of the mod as a:

### Situational Awareness Timer

not a:

### Guaranteed Unspotted Indicator

---

## What the Mod Does

The mod:

* Reacts to the standard Sixth Sense alert
* Plays an exact 12-second audio sequence
* Provides an audible elapsed-time reference
* Helps reduce the need to manually count during combat

---

## What the Mod Does Not Do

The mod does not:

* Detect which enemy spotted you
* Determine whether an enemy currently has vision of you
* Detect when line of sight is broken
* Read hidden gameplay information
* Calculate your real-time spotting state
* Confirm when your vehicle becomes unspotted
* Perform any automated combat action

It simply plays a fixed 12-second audio sequence when Sixth Sense activates.

---

## Troubleshooting

If the sound does not play:

### `.wotmod` Method

Confirm the file is inside:

```text
mods\<current_game_version>\
```

### Manual Method

Confirm the file is named:

```text
sixthSense.mp3
```

and located inside:

```text
res_mods\<current_game_version>\audioww\
```

Also check:

* `User sound` is selected in the Sixth Sense sound setting
* You are using the current World of Tanks version folder
* World of Tanks has been restarted
* No other Sixth Sense or audio mod is overriding the sound

---

## Uninstallation

### `.wotmod`

Delete the mod from:

```text
mods\<current_game_version>\
```

### Manual Method

Delete:

```text
res_mods\<current_game_version>\audioww\sixthSense.mp3
```

Restart World of Tanks.

The standard Sixth Sense sound will be restored.

---

## Repository Description

> World of Tanks Sixth Sense audio mod featuring an exact 12-second ticking timer with `.wotmod` and manual installation support.
