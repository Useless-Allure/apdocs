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
        - [ ] Implementation
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

## Expansion to Entrance Rando

!!! greysondn "greysondn - Entrance Rando"
    Right now, entrance rando is typically 1:1. But what we're seeing with
    Spyro is more like 1:1:1, which gamefreq0 represented by splitting
    it up 1:1 + 1:1 and then doing custom logic over those.
    
    It feels like this is a generalizable problem. I've not quite pieced
    together the exact data here, however, so... it has to wait. It's
    just an observation right now.

12 July 2026. Can be found in the 1-1 chat with gamefreq0 by searching for `45c77609-b04e-4f6e-9d13-119bd118eb16` if you have access (all two people in the world).