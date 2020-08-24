---
layout: default
title: gregcman's Homepage
---
***
<a href="/">
<img src="images/800px-Surreal_number_tree.svg2.png"
     alt="Profile Picture"
     style="float:right; border-radius:10px; margin:20px; height:240px;" />
</a>
# Contents
1. [Contents](#contents)
2. [Links](#links)
3. [Projects](#projects)
4. [My Setup](#my-setup)
5. [Note Taking](#note-taking)
6. [Some Things I Like](#some-things-i-like)
7. [Other Links](#other-links)
8. [LISP](#lisp)

***

# Links

- [Email](mailto:gregoriomanabat@gmail.com)
- [GitHub](https://github.com/gregcman)
- [YouTube](https://www.youtube.com/channel/UCqmBXq8zxsmU5YSQWGRUHgA)
- [LinkedIn](https://www.linkedin.com/in/gregorio-manabat/)

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
      2. An LRU cache.
      3. The disk, or database.
- notes
  - I took a lot of notes over the years but they were scattered everywhere, across google docs, google keep, Samsung notes, evernote, apple notes, custom locations, and emails, so it became extremely difficult to reflect and review progress. This system consolidates all of it into a single file sorted by time.  
    - Makes extensive usage of [timestamps](https://common-lisp.net/project/local-time/manual.html) as well as [XML and HTML parsers](https://github.com/Shinmera/plump).
    - I fed the output file into [GPT-2](https://github.com/openai/gpt-2) which created an eerie caricature likeness of me. GPT-2 Also seems to have come up with some legitimate original ideas by remixing my own words, although most of it was less coherent.
    
- [cl-c-parse](https://github.com/gregcman/cl-c-parse)
  - Prototype of a C parser in Common Lisp, that is generated from Lex and Yacc specifications. It is correct, but very slow.
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
  - GPU accelerated grid-of-characters user interface.
    - Similar to [alacritty](https://github.com/alacritty/alacritty), the GPU terminal emulator.
    - Very dense data transfer to the GPU, each character is just 4 bytes.
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
  - [Completely fair scheduling](https://en.wikipedia.org/wiki/Completely_Fair_Scheduler), an algorithm used in the Linux kernel to schedule processes by priority.
- [wfc](https://github.com/gregcman/sucle/blob/wfc/src/sucle/wfc.lisp)
  - A simple implementation of the [wavefunction collapse algorithm](https://github.com/mxgmn/WaveFunctionCollapse) which is a constraint solving system used for n-dimensional texture synthesis.
  - Extremely slow for voxels.
  - Turns out procedural content generation is hard and requires a lot of compute, whether that be on the cloud or in the minds of many creators.
- [cl-telegram](https://github.com/gregcman/cl-telegram)
  - Use the Telegram web API to poll for updates and send messages.
    - API generated by parsing the [Telegram documentation](https://core.telegram.org/bots/api) (HTML)
- [cl-nbt](https://github.com/pull-request-perhaps/cl-nbt) [Fork]
  - Add system to deal with `.mca` files and make the algorithm simpler and more general.
- [freecodecamp](https://github.com/gregcman/freecodecamp)
  - Solutions for the freeCodeCamp course.
  - Did the main tutorials, but skipped the larger projects. So each individual CSS, HTML, Node, JavaScript, React, Sass, Jquery, and Redux exercise, but didn't combine the pieces into a larger project.
- [gregcman.github.io](https://github.com/gregcman/gregcman.github.io)
  - Markdown sprinkled with HTML.
  - Uses [Jekyll](https://jekyllrb.com/).
- [lisp-in-small-pieces](https://github.com/gregcman/lisp-in-small-pieces) [Fork]
  - A [Scheme](https://en.wikipedia.org/wiki/Scheme_(programming_language)) compiler and bytecode interpreter from the book [Lisp In Small Pieces](https://wiki.c2.com/?LispInSmallPieces).
- [ridikulisp](https://github.com/gregcman/ridikulisp)
  - A very tiny Turing complete language which is easy to extend and implement.
    - Not a [Turing tarpit](https://en.wikipedia.org/wiki/Turing_tarpit).
    - Inspired by LISP and [bitbitjump](https://esolangs.org/wiki/BitBitJump).
- [llvm-for-cl](https://github.com/gregcman/llvm-for-cl)
  - Basic compiler from s-expressions to assembly using LLVM.


***
# My setup
- OS: [Ubuntu](https://ubuntu.com/)
- Window manager: [i3](https://i3wm.org/) and [i3bar](https://i3wm.org/i3bar/)
- Editor: [Emacs](https://www.gnu.org/software/emacs/) with [SLIME](https://common-lisp.net/project/slime/), [paredit](https://www.emacswiki.org/emacs/ParEdit), [autocomplete](https://github.com/auto-complete/auto-complete), and [ac-slime](https://github.com/purcell/ac-slime).
- Any terminal
- Common Lisp: [SBCL](http://www.sbcl.org/)
- Version control: [git](https://en.wikipedia.org/wiki/Git), [smartgit](https://www.syntevo.com/smartgit/)
- [grep](https://en.wikipedia.org/wiki/Grep), [pkill](https://en.wikipedia.org/wiki/Pkill), [htop](https://hisham.hm/htop/)
- Browser: [Firefox](https://www.mozilla.org/en-US/)
- File Manager: [pcmanfm](https://wiki.lxde.org/en/PCManFM) in dual-pane mode
- Quick Notes: copy paper on a clipboard, or [Google Keep](https://keep.google.com)

In i3, I'll divide my desktops according to what task I'm doing.

Each desktop is split into two halves, and within each half is multiple i3-tabs.

Example:

- Desktop 1: Programming
  - Left side tabs:
    - Firefox
      - [CLHS](http://clhs.lisp.se/)
      - [Github](https://github.com/)
      - [StackOverflow](https://stackoverflow.com/)
    - SmartGit
    - terminal
    - Emacs running SLIME using SBCL
    - Some Emacs buffers
    - pcmanfm
  - Right side tabs:
    - terminal
    - Multiple Emacs buffers
- Dekstop 2: Note taking
  - Left side tabs:
    - pcmanfm
    - SmartGit
  - Right side tabs:
    - Emacs
    - terminal
- Desktop 3: Schoolwork
  - firefox
    - Email
    - School website
    - LibreOffice
- Desktop 4: other
  - ...

I usually:
- Drag files from pcmanfm on the left side to the right side where there is:
  - Emacs
  - The terminal
- Open the terminal from pcmanfm on the left side, upon which the terminal is moved to the right side.
- Edit code on the right and on the left:
  - Test the code in the REPL
  - Look up libraries/documentation/algorithms for the code

When putting the computer to sleep I open a random terminal and put it to sleep. I rarely ever turn my computer off, last time I checked it was on for 60 days straight.

***
## Note taking

After testing many different systems and services, struggling, and looking up what [systems others used](https://news.ycombinator.com/item?id=22276184), I converged upon the system I use currently:

1. One-off notes/graphical: [Pen](https://uniballco.com/uni-products/signo-207/), copy paper, and clipboard. 
   1. Try to write the date on the paper.
   2. Put the paper in a dedicated pile when finished. 
   3. Paper is scanned later with a portable scanner or phone camera.
2. Whenever a random thought strikes me
  - Open my phone and type it in.
    - Google Keep is currently the least evil service.
      - Evernote has this wacky HTML/XML format that I had to write a custom printer for.
      - Samsung notes and Apple notes are the most evil. Vendor Lock-In, no easy way to export. Dealing with these was extremely tedious.
3. Longer more in-depth ideas: pcmanfm, SmartGit, Emacs, SBCL, SLIME, [local-time](https://common-lisp.net/project/local-time/manual.html)
  - A single file called `linear.lisp`. It is alternating `local-time:timestamp` objects and Common Lisp objects. The `local-time:timestamp` objects delineate the boundaries of each note. Usually there is just a single string between `local-time:timestamp` objects.
    - When adding a new note, run `(local-time:now)` in the REPL, paste the result at the end, and create a new string following it.

Using Google Keep:
1. Download google archive with Keep notes
2. Run it through [KeepToText](https://github.com/HardFork/KeepToText)
3. Run it through the custom `notes` system I created that integrates it with my other notes.

  
***
## Some things I like:
- [Hacker News](https://news.ycombinator.com/)
- [LessWrong](https://www.lesswrong.com/)
- [Wikipedia](https://www.wikipedia.org/)
- [xkcd](https://xkcd.com/)
- [Existential Comics](http://existentialcomics.com/)
- [SMBC](https://www.smbc-comics.com/)
- [FunnyJunk](https://funnyjunk.com/)
- [ethoslab](https://www.youtube.com/channel/UCFKDEp9si4RmHFWJW1vYsMA)
- [TwoMinutePapers](https://www.youtube.com/user/keeroyz)
- [Universal Intelligence: A Definition of Machine Intelligence](https://arxiv.org/abs/0712.3329)
- [Antifragile](https://en.wikipedia.org/wiki/Antifragile)
- [Infinity and the Mind](https://en.wikipedia.org/wiki/Infinity_and_the_Mind)
- [Pareto efficiency](https://en.wikipedia.org/wiki/Pareto_efficiency)
- [Myers–Briggs Type Indicator (MBTI)](https://en.wikipedia.org/wiki/Myers%E2%80%93Briggs_Type_Indicator)
- [OCEAN model](https://en.wikipedia.org/wiki/Big_Five_personality_traits)
- [Surreal number](https://en.wikipedia.org/wiki/Surreal_number)
- [Simulation hypothesis](https://en.wikipedia.org/wiki/Simulation_hypothesis)
- [List of cognitive biases](https://en.wikipedia.org/wiki/List_of_cognitive_biases)
- [Dunbar's number](https://en.wikipedia.org/wiki/Dunbar%27s_number)
- [Brute-force search](https://en.wikipedia.org/wiki/Brute-force_search)
- [Rationality: From AI to Zombies](https://wiki.lesswrong.com/wiki/Rationality:_From_AI_to_Zombies)
- [Minimax](https://en.wikipedia.org/wiki/Minimax)
- [Single point of failure](https://en.wikipedia.org/wiki/Single_point_of_failure)
- [Project management](https://en.wikipedia.org/wiki/Project_management)
- [Turtles all the way down](https://en.wikipedia.org/wiki/Turtles_all_the_way_down)
- [Fractal](https://en.wikipedia.org/wiki/Fractal)
- [Focus Your Uncertainty](https://www.lesswrong.com/posts/GJ4ZQm7crTzTM6xDW/focus-your-uncertainty)
- [Hunter x Hunter](https://en.wikipedia.org/wiki/Hunter_%C3%97_Hunter)
- [SCP Foundation](http://www.scp-wiki.net/)
- [tv tropes](https://tvtropes.org/)
- [Metastability](https://en.wikipedia.org/wiki/Metastability)
- [Bayes' theorem](https://en.wikipedia.org/wiki/Bayes%27_theorem)
- [generative adversarial network (GAN)](https://en.wikipedia.org/wiki/Generative_adversarial_network)
- [Orthogonality](https://en.wikipedia.org/wiki/Orthogonality_(programming))
- [Master–slave morality](https://en.wikipedia.org/wiki/Master%E2%80%93slave_morality)
- [Meta-circular evaluator](https://en.wikipedia.org/wiki/Meta-circular_evaluator)
- [Feedback](https://en.wikipedia.org/wiki/Feedback)

***

# Other Links

- [Twitter](https://twitter.com/gregcman1)
- [Discord](https://discord.gg/rj9gUSm)
- [Instagram](https://www.instagram.com/gregcman3/)
- [itch.io](https://gregcman.itch.io/)
- [Quora](https://www.quora.com/profile/Greg-C-Man)
- [StackOverflow](https://stackoverflow.com/users/11832878/greg-c-man)
- [Reddit](https://www.reddit.com/user/gregcman)

***
## LISP

Common LISP allows an individual programmer to prototype faster than any other programming language. It is the language of choice if you an an individual programmer. 
