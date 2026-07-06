!!! greysondn "Flying Blind"
    These docs need gamefreq0 to sit with me, but I wanted to at least
    write down what I believe I know.

---

[TOC]

---

# The Basics

## Latest AP World

Right now, the latest hotfix version is avaialable in the Archipelago discord here:
[https://discord.com/channels/731205301247803413/1281652479779536958/1508309230438973641](https://discord.com/channels/731205301247803413/1281652479779536958/1508309230438973641)

The Archipelago discord itself is linked from the top right corner of the Archipelago homepage: [https://archipelago.gg/](https://archipelago.gg/)

## Documentation

The game info page is in gamefreq0's repository here:  
[https://github.com/gamefreq0/Archipelago/blob/spyro/worlds/spyro/docs/en_Spyro%20the%20Dragon.md](https://github.com/gamefreq0/Archipelago/blob/spyro/worlds/spyro/docs/en_Spyro%20the%20Dragon.md)

The setup docs are in gamefreq0's repository here:
[https://github.com/gamefreq0/Archipelago/blob/spyro/worlds/spyro/docs/guide_en.md](https://github.com/gamefreq0/Archipelago/blob/spyro/worlds/spyro/docs/guide_en.md)

## Optional Poptracker

Leaddybug has designed a boss MacGuffin and Goal tracker, available here:  
[https://github.com/LeaddyBug/Spyro-1-Boss-MacGuffin-and-Goal-Tracker](https://github.com/LeaddyBug/Spyro-1-Boss-MacGuffin-and-Goal-Tracker)

!!! greysondn "Why isn't there more to the poptracker?"
    The codebase is undergoing an overhaul since August of 2025. I am
    actually the person responsible for that overhaul. I apologize.
    Anyway, a good poptracker is awaiting some resources I can give
    with less effort once the overhaul is done. I wanted to lower the
    labor threshold for poptracker creators in general.

# Known Gotchas

## Game Version

Must be Spyro the Dragon (USA) for the Playstation 1.

Checksum the `.bin` file. (Replace `spyro.bin` with the name of your file in the following directions.)

In **Windows 10/11**, this is done via `certutil` using a command prompt:

```batch
certutil -hashfile spyro.bin MD5
```

In **most Linux distros**, this is done via `md5sum`:

```bash
md5sum spyro.bin
```

The expected sum is:

```
387185f71cd0043fd75a19521dc75104
```

You can learn more about this on the redump page for that disc if it's relevant to you: [http://redump.org/disc/576/](http://redump.org/disc/576/). This is also a place to grab a cue sheet if you're missing one (a `.cue` file with the bin).

We do not support any other checksum for that `.bin` file at this time.

!!! greysondn "Europe? Australia?"
    I want to do this and gamefreq0 isn't opposed. However, the first goal
    is to get the formats for everything stable and USA running again
    first.

## PS1 Bios

The only viable bios seems to be a USA PS1 bios from the original hardware. It's not impossible that any for the actual PS1 would work if it can boot the game, but we know for sure that the PS3 version of the PS1 bios does not work. We believe this has to do with how the bios initializes RAM and some data that the bizhawk connector itself needs.

## Emulator Core

Gamefreq0 is a linux developer. He only has the Nymashock core available for development and testing. You are best off using Nymashock to play this APWorld.

!!! greysondn "Duckstation?"
    This is a long and storied history, but the simplest version is that
    Duckstation is hostile to Linux packaging, so it's unreasonable to
    expect Gamefreq0 to support it. Actually; Gamefreq0 and I sat and talked
    about this at some point. We aren't opposed to Duckstation support,
    but we've no intention of doing it ourselves. In theory, the underlying
    libs I've been working on should make this easier, but I don't plan
    to write a Duckstation implementation for them, either.
    
    This isn't the only thing Duckstation did. However, the leader of that
    team is pretty... spirited... when people have criticisms about it all.
    I think he'll agree it's fair to say he's had it with Linux users and
    it's reasonable that Linux users would see that and decide not to
    engage with it.
