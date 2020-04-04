---
layout: default
title: Home
---
***

# Links

- [Github](https://github.com/gregcman)
- [Youtube](https://www.youtube.com/channel/UCqmBXq8zxsmU5YSQWGRUHgA)

***

# Projects

- [sucle](https://github.com/gregcman/sucle)
  - The infinite voxel editor and walking simulator in Common Lisp. Create and explore intricate procedural shapes that stretch on for hundreds of thousands of miles.
    - Uses model-view-controller, flood fill, convolutions, vector algebra, frustum culling, and others. 
  - <iframe src="https://ghbtns.com/github-btn.html?user=gregcman&repo=sucle&type=star&count=true" frameborder="0" scrolling="0" width="170px" height="20px"></iframe>
- [lem](https://github.com/cxxxr/lem) [Contributor]
  - Find and fix some minor bugs, such as scrolling and job processing.
  - Implement an [interactive frontend](https://github.com/gregcman/sucle/tree/master/src/lem-opengl) that allows dragging to resize windows, double and triple clicking, and dragging and dropping files.
  - Created a [simplified version](https://github.com/gregcman/minilem) in the spirit of [microemacs](https://github.com/torvalds/uemacs).
  - <iframe src="https://ghbtns.com/github-btn.html?user=cxxxr&repo=lem&type=star&count=true" frameborder="0" scrolling="0" width="170px" height="20px"></iframe>
- [crud](https://github.com/gregcman/sucle/tree/master/src/crud)
  - Persistent key-value storage for Common Lisp objects.
  - **C**reate, **R**ead, **U**pdate, **D**elete. 
    - Use either [sqlite](https://www.sqlite.org/index.html) or a directory of files as storage. 
    - Optionally use transactions to make it faster.
- [voxel-chunks](https://github.com/gregcman/sucle/blob/master/src/sucle/voxel-chunks.lisp)
  - A tiered cache system for voxels.
    - Levels:
      1. 3D array that can pin memory.
      2. A [mru](https://en.wikipedia.org/wiki/Cache_replacement_policies#Most_recently_used_(MRU)) (most recently used) cache.
      3. The disk, or database.
- notes
  - I took a lot of notes over the years but they were scattered everywhere, across google docs, google keep, samsung notes, evernote, apple notes, custom locations, and emails, so it became extremely difficult to reflect and review progress. This system consolidates all of it into a single file sorted by time.  
    - Makes extensive usage of [timestamps](https://common-lisp.net/project/local-time/manual.html) as well as [XML and HTML parsers](https://github.com/Shinmera/plump).
    - I fed the output file into [GPT-2](https://github.com/openai/gpt-2) which created an eerie caricature likeness of me. GPT-2 Also seems to have come up with some legitimate original ideas by remixing my own words, although most of it was less coherent.
    
- [cl-c-parse](https://github.com/gregcman/cl-c-parse)
  - Prototype of a c parser in common lisp, that is generated from lex and yacc specifications. It is  correct, but very slow.
  - <iframe src="https://ghbtns.com/github-btn.html?user=gregcman&repo=cl-c-parse&type=star&count=true" frameborder="0" scrolling="0" width="170px" height="20px"></iframe>
- [sucle-multiprocessing](https://github.com/gregcman/sucle/tree/master/src/sucle-multiprocessing)
  - A job system.
    - Similar to the API of [Unity](https://unity.com/)'s job system.
    - Created because there were no Common Lisp job processing systems where the task itself was an object that could be queried or stopped.
- [opengl](https://github.com/gregcman/sucle/tree/master/src/opengl)
  - Implementation of the basic OpenGL functions and a thin layer that provides compatibility across GLSL versions and OpenGL versions.
    - Similar in spirit to [ANGLE](https://github.com/google/angle). I have not checked the benchmarks.
    - Compatibility layers created so many people could use sucle.
- [text-subsystem](https://github.com/gregcman/sucle/tree/master/src/text-subsystem)
  - GPU accelated grid-of-characters user interface.
    - Similar to [alacritty](https://github.com/alacritty/alacritty), the gpu terminal emulator.
    - Very dense data transfer to the gpu, each character is just 4 bytes.
      - Compared to the naive polygon with texture and color attributes, which is 4 vertices with 2 texture coordinates each and 2 colors each.
      - 128 bytes = 4*((sizeof(float) * 2) + (sizeof(float) * 3 * 2)). 128/4= 32 times less data transfer.
- [a-sound-system](https://github.com/gregcman/a-sound-system)
  - Audio streaming/playing library that uses [FFmpeg](https://ffmpeg.org/), [libsndfile](http://www.mega-nerd.com/libsndfile/), and [OpenAL](https://www.openal.org/)
- [project-euler](https://github.com/gregcman/project-euler)
  - Solving [math problems](https://projecteuler.net/) in Python and Common Lisp.
- [aabbcc](https://github.com/gregcman/sucle/blob/master/src/aabbcc/aabbcc.lisp)
  - A simple 3D collision system.
  - 3D rasterization of lines.
- [sucle-serialize](https://github.com/gregcman/sucle/tree/master/src/sucle-serialize)
  - An object serializer and deserializer for Common Lisp.
    - Sort of like python's [pickle](https://docs.python.org/3/library/pickle.html). 
- [cl-cfs-scheduler](https://github.com/gregcman/cl-cfs-scheduler)
  - [Completely fair scheduling](https://en.wikipedia.org/wiki/Completely_Fair_Scheduler), an algorithm used in the linux kernel to schedule processes by priority.
- [wfc](https://github.com/gregcman/sucle/blob/wfc/src/sucle/wfc.lisp)
  - A simple implementation of the [wavefunction collapse algorithm](https://github.com/mxgmn/WaveFunctionCollapse) which is a constraint solving system used for n-dimensional texture synthesis.
  - Extremely slow for voxels.
  - Turns out procedural content generation is hard and requires a lot of compute, whether that be on the cloud or in the minds of many creators.
- [cl-telegram](https://github.com/gregcman/cl-telegram)
  - Use the telegram web api to poll for updates and send messages.
    - API generated by parsing the [telegram documentation](https://core.telegram.org/bots/api) (HTML)
- [cl-nbt](https://github.com/pull-request-perhaps/cl-nbt) [Fork]
  - Add system to deal with .mca files and make the algorithm simpler and more general.
- [freecodecamp](https://github.com/gregcman/freecodecamp)
  - Solutions for the freeCodeCamp course.
  - Did the main tutorials, but skipped the larger projects. So each individual CSS, HTML, Node, Javascript, React, Sass, Jquery, Redux, but didn't combine the pieces into a larger project.
- [gregcman.github.io](https://github.com/gregcman/gregcman.github.io)
  - Markdown sprinkled with HTML, especially for the github star-count buttons.
  - Uses [Jekyll](https://jekyllrb.com/).
- [lisp-in-small-pieces](https://github.com/gregcman/lisp-in-small-pieces) [Fork]
  - A [Scheme](https://en.wikipedia.org/wiki/Scheme_(programming_language)) compiler and bytecode interpreter from the book [Lisp In Small Pieces](https://wiki.c2.com/?LispInSmallPieces).
- [ridikulisp](https://github.com/gregcman/ridikulisp)
  - A very tiny turing complete language which is easy to extend and implement, it is not a turing tarpit. Inspired by LISP and [bitbitjump](https://esolangs.org/wiki/BitBitJump).
- [llvm-for-cl](https://github.com/gregcman/llvm-for-cl)
  - Basic compiler from s-expressions to assembly using LLVM.

***
## My mixed opinion of LISP

LISP is not economically or socially viable because it is the most rapid prototyping language available.<br>
It is indispensable if you:
1. Enjoy programming itself
2. Have a unique problem at hand with limited computing power.

LISP is the essence of unbridled individualism.
I, being an american, was raised on rugged individualism. Thus, LISP appeals to me and it saddens me that this cherished art is dying.

It also pains me to say that Individualism is overrated. Individualism does not scale. The bigger your operation, the more it converges on the hard sciences and leaves little room for hand-wavy self expression.

***
## My setup
- OS: [Ubuntu](https://ubuntu.com/)
- Window manager: [i3](https://i3wm.org/) and [i3bar](https://i3wm.org/i3bar/)
- Editor: [emacs](https://www.gnu.org/software/emacs/) with [SLIME](https://common-lisp.net/project/slime/), [paredit](https://www.emacswiki.org/emacs/ParEdit), [autocomplete](https://github.com/auto-complete/auto-complete), and [ac-slime](https://github.com/purcell/ac-slime).
- Any terminal
- Common Lisp: [SBCL](http://www.sbcl.org/)
- Version control: [git](https://en.wikipedia.org/wiki/Git), [smartgit](https://www.syntevo.com/smartgit/)
- [grep](https://en.wikipedia.org/wiki/Grep), [pkill](https://en.wikipedia.org/wiki/Pkill), [htop](https://hisham.hm/htop/)
- Browser: [firefox](https://www.mozilla.org/en-US/)
- File Manager: [pcmanfm](https://wiki.lxde.org/en/PCManFM)
- Quick Notes: copy paper on a clipboard, or [Google Keep](https://keep.google.com)

In i3, I'll divide my desktops according to what task I'm doing.

Each desktop is split into two halves, and within each half is multiple i3-tabs.

Example:

- Desktop 1: Programming
  - Left side tabs:
    - firefox
      - [CLHS](http://clhs.lisp.se/)
      - [github](https://github.com/)
      - [stackoverflow](https://stackoverflow.com/)
    - smartgit
    - terminal
    - Emacs running SLIME using SBCL
    - Some Emacs editing tabs
    - pcmanfm
  - Right side tabs:
    - terminal
    - Multiple Emacs editing files. 
- Dekstop 2: Note taking
  - Left side tabs:
    - pcmanfm
    - smartgit
  - Right side tabs:
    - Emacs
    - terminal
- Desktop 3: Schoolwork
  - firefox
    - email
    - school website
    - LibreOffice
- Desktop 4: other
  - ...

***

# Other Links

- [Twitter](https://twitter.com/gregcman1)
- [Discord](https://discord.gg/rj9gUSm)
- [Instagram](https://www.instagram.com/gregcman3/)
- [itch.io](https://gregcman.itch.io/)
- [Quora](https://www.quora.com/profile/Greg-C-Man)
- [Stackoverflow](https://stackoverflow.com/users/11832878/greg-c-man)
- [Reddit](https://www.reddit.com/user/gregcman)
- [Linkedin](https://www.linkedin.com/in/gregorio-manabat/)