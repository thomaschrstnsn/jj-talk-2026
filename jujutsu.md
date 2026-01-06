---
theme:
  name: catppuccin-frappe
  override:
    footer:
      style: template
      left:
        image: ./assets/jj.png
      center: '**Introduction** to _Jujutsu_'
      right: "{current_slide} / {total_slides}"
      height: 3
    palette:
      classes:
        noice:
          foreground: "FF8C00"
---
<!-- no_footer -->
<!-- newlines: 6 -->

![image:width:30%](./assets/jj.png)

<!-- alignment: center -->
**Introduction** to <span class="noice">_Jujutsu_</span>

<!-- alignment: center -->

## <span class="noice">_**Thomas Fisker Christensen**_</span>

<!-- end_slide -->

# WHAT IS <span class="noice">_Jujutsu_</span>?

<!-- newlines: 6 -->

- it is a powerful version control system for software projects.
- initially developed by _Martin von Zweigbergk_ (@ Google)
  - now part of the jj-vcs org on github
- used at Google, being rolled out for _General Availability_ in [the beginning of 2026](https://www.youtube.com/watch?v=v9Ob5yPpC0A)
  - Google use a different backend (not git) for their monorepo

<!-- end_slide -->

# FIVE BIG IDEAS

<!-- newlines: 6 -->

- automatic snapshotting 🎰
- atomatic rebasing ♻️
- anonymous first 🎭
- first class conflicts ⚠️
- git compatible 

<!-- end_slide -->

# AUTOMATIC SNAPSHOTTING

- everything is always "checked" in (no dirty copy)
  - means you are always free to move around
  - everything is always comitted
    - _commit_: way of storing your changes, not necessarily ready to share (free to return to it and refine later)
  - every (non-ignored) file is always added
  - undeniably simpler™
    - contrast with git:
      - branch (naming is hard)
      - stage before commit
      - commit

<!-- end_slide -->

# AUTOMATIC REBASING

<!-- jump_to_middle -->

> constantly in the middle of an interactive rebase

```mermaid +render
---
config:
  themeVariables:
    'git0': '#00F000'

  gitGraph:
    showBranches: false
---
gitGraph
   commit
   commit id: "alpha" type: HIGHLIGHT
   commit
   commit id: "beta" type: HIGHLIGHT
   commit
   branch thought
   commit id: "gamma"
   commit
   commit
   checkout main
   commit id: "sigma" type: HIGHLIGHT
```

<!-- end_slide -->

# ANONYMOUS FIRST

- branches:
  - name when you are ready to share with others
- changes/commits:
  - describe when you are sure should how you want to "tell your story"

<!-- end_slide -->

# FIRST CLASS CONFLICTS

- conflicts are stored in your tree and can be solved later, in one go or in many smaller attempts.
  - stored in commits
    - the inputs to the merge
    - cheap to recalculate what a conflict is
      - re-evaluate if it has been resolved
  - jump around and do the work and resolve conflicts when it suits you
    - contrast: in git conflicts are "stop the world" events 😢

<!-- end_slide -->

# aside

![image:width:30%](assets/2026-01-06-20-57-19.png)
<!-- alignment: center -->
[mergiraf](https://mergiraf.org/)
  
resolving conflicts at 60 km/h

<!-- end_slide -->

# [mergiraf](https://mergiraf.org/)

## Language semantics guided merge tool 🪄✨
  
- Rust (`*.rs`)
- Javascript (`*.js, *.jsx, *.mjs`), TypeScript (`*.ts, *.tsx`)
- C/C++ (`*.c, *.h, *.cc, *.hh, *.cpp, *.hpp, *.cxx, *.hxx, *.c++, *.h++, *.mpp, *.cppm, *.ixx, *.tcc`)
- C# (`*.cs`)
- Python (`*.py`)

Supported out of the box in _Jujutsu_:

```bash
jj resolve --tool mergiraf
```

<!-- end_slide -->

![image:width:50%](assets/mergiraf1.png)
<!-- end_slide -->

![image:width:50%](assets/mergiraf2.png)
<!-- end_slide -->

![image:width:50%](assets/mergiraf3.png)
<!-- end_slide -->

<!-- jump_to_middle -->
<!-- alignment: center -->

back to _Jujutsu_
<!-- end_slide -->

# git backend

<!-- jump_to_middle -->
- <span class="noice">jj</span> is transparent to others _(git users)_
- git is ubiquitous
- git has "ok"-ish UX

<!-- end_slide -->

# Stockholm syndrome? 🇸🇪 🫎

<!-- jump_to_middle -->
> a _psychological_ coping mechanism where **hostages** or **abuse victims** develop _positive feelings_, _empathy_, or even _loyalty_ toward their **captors** or **abusers**

- who here uses **vanilla** commandline git󰊢?
  - **(without any aliases or helper scripts)**?
- blink twice if you are being held against your will 😉

<!-- end_slide -->

# WHAT I LOVE ❤️ _FLUIDITY OF MOVING AROUND_ 🪾

- try different approaches, capture them all in _VCS_ (not just in editor undo history)
<!-- list_item_newlines: 1 -->
- branch 
- squash 🥒
- split 🪓
- abort ❌
- rearrange 
- rebase 󰡓
- edit 
- duplicate 
<!-- list_item_newlines: 2 -->
- leads to **fearless** _iteration/experimentation_ 🧪⚗️
  - without ever getting in the way ❤️🙏

<!-- end_slide -->

# demo

![image:width:50%](assets/2026-01-06-22-12-41.png)

<!-- alignment: center -->

using [jjui](https://github.com/idursun/jjui)

<!-- end_slide -->

# LINK DUMP

<!-- include: links.md -->
