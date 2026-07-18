---

[TOC]

---

# Scratchpad

A place to capture the ideas we've had or had suggested to us.

## Todo List for `rewrite-1` branch

!!! greysondn "greysondn - my tasklist"
    This is just a view of what I can see. It may fall out of date. It may
    shorten and/or expand.

** Last known update: 13 July 2026 **

- [ ] Data files
    - [X] *Memory addresses*
        - [X] Design
        - [X] Implementation
            - `data/memory/`
    - [X] Basic version of *regions*
        - [X] Design
        - [X] Implementation
            - `data/regions/`
    - [X] Basic placement of *locations* (eggs, dragons)
        - [X] Design
        - [X] Implementation
            - this is part of `data/regions/`
    - [X] Basic version of *items*
        - [X] Design
        - [X] Implementation
            - `data/items/`
    - [X] Basic version of *connections*
        - [X] Design
        - [X] Implementation
            - this is part of `data/regions/`
    - [ ] lightweight file to use in identifying Spyro version
        - [ ] Design
        - [ ] Implementation 
- [ ] APpetite
    - [ ] Parse and represent data clauses
        - [ ] `meta`
        - [ ] `entrance_rando`
        - [ ] `items`
        - [ ] `memory`
        - [ ] `regions`
        - [ ] `patches`
        - [ ] common/important subclauses
            - [ ] `sources`
            - [ ] `guard`
            - [ ] `callback`
    - [ ] full internal representation
    - [ ] compat client interface base for AP
    - [ ] release APpetite 0.1
- [ ] Feature parity, release, and modernization
    - [ ] Proper archipelago client built over APpetite
    - [ ] Implemenration of dyamic region connections
        - [ ] world to starting hub
        - [ ] starting hub to balloonist
    - [ ] restore portal sanity
    - [ ] dangling updates to become main development branch
    - [ ] push into gamefreq0's repo
    - [ ] release α1
    - [ ] update to current AP standards
    - [ ] release α2
- [ ] Post-release
    - [ ] APpetite
        - [ ] Data exporters
            - [ ] Poptracker
            - [ ] Memory map

## Callbacks List

!!! greysondn "greysondn - Callbacks"
    I just need a good view of what all the callbacks are as we
    decide/identify them, nothing complex here.

### Hook points

Hook points take the name format of `[time]_[verb]`.

* items
    * `pre_receive`
    * `on_receive`
    * `post_receive`
    * `on_hint`
* locations
    * `pre_obtain`
    * `on_obtain`
    * `post_obtain`
    * `on_collect` - called when a player collects the location
    * `on_scout`
    * `on_hint`
* connections
    * `on_connect` - called during generation when the connection is actually connected.


### Callbacks

Actual callbacks, per object.

- `nop` - do nothing (default)
- `write_memory` - label on tin
- `increment_memory` - label on tin
- `decrement_memory` - label on tin
- `ensure_memory` - label on tin

## Guards List

!!! greysondn "greysondn - Ad Hoc Development"
    I've been developing this very, very ad-hoc, so I need a list of what
    I've decided on the fly.

```yaml
-
    type: always
-
    type: and
    params:
        next: [list[GUARD]]
-
    type: has_item
    params:
         name: [str: ITEM NAME]
         count: [uint]
-
    type: memory_equals
    params:
        name: [str: MEMORY NAME]
        value: [any: LEGAL VALUE]
-
    type: never
-
    type: not
    params:
        next: [GUARD]
-
    type: or
    params:
        next: [list[GUARD]]
```

## QOL changes to the base game

* Nestor's dialogue in Artisans is now skippable

## Possible regressions

* Statue head checks were originally nop'ing out 4 bytes.

## Locations by ID

```yaml
"Artisans":         10
"Stone Hill":       11
"Dark Hollow":      12
"Town Square":      13
"Toasty":           14
"Sunny Flight":     15
"Peace Keepers":    20
"Dry Canyon":       21
"Cliff Town":       22
"Ice Cavern":       23
"Doctor Shemp":     24
"Night Flight":     25
"Magic Crafters":   30
"Alpine Ridge":     31
"High Caves":       32
"Wizard Peak":      33
"Blowhard":         34
"Crystal Flight":   35
"Terrace Village":  41
"Misty Bog":        42
"Tree Tops":        43
"Metalhead":        44
"Wild Flight":      45
"Dream Weavers":    50
"Dark Passage":     51
"Lofty Castle":     52
"Haunted Towers":   53
"Jacques":          54
"Icy Flight":       55
"Gnasty's World":   60
"Gnorc Cove":       61
"Twilight Harbor":  62
"Gnasty Gnorc":     63
"Gnasty's Loot":    64
```

## Thoughts

###  Expansion to Entrance Rando

!!! greysondn "greysondn - Entrance Rando"
    Right now, entrance rando is typically 1:1. But what we're seeing with
    Spyro is more like 1:1:1, which gamefreq0 represented by splitting
    it up 1:1 + 1:1 and then doing custom logic over those.
    
    It feels like this is a generalizable problem. I've not quite pieced
    together the exact data here, however, so... it has to wait. It's
    just an observation right now.

12 July 2026. Can be found in the 1-1 chat with gamefreq0 by searching for `45c77609-b04e-4f6e-9d13-119bd118eb16` if you have access (all two people in the world).