---
theme:
  name: catppuccin-latte
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
          foreground: #FF8C00
---
<!-- no_footer -->
<!-- newlines: 6 -->

![image:width:30%](./assets/jj.png)

<!-- alignment: center -->
**Introduction** to <span class="noice">_Jujutsu_</span>

<!-- alignment: center -->

<span style="color: blue">Thomas Fisker Christensen</span>

<!-- end_slide -->

# WHAT IS _Jujutsu_?

<!-- newlines: 6 -->

- it is a powerful version control system for software projects.
- initially developed by Martin von Zweigbergk (employed at Google)
  - now part of the jj-vcs org on github
- used at Google, being rolled out for _General Availability_ in [the beginning of 2026](https://www.youtube.com/watch?v=v9Ob5yPpC0A)
  - using a different backend (not git) for their monorepo

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
  - commit: way of storing your changes, not necessarily ready to share (free to return to it and refine later)
  - every (non-ignored) file is always added
  - undeniably simpler™
    - contrast with:
      - branch (naming is hard)
      - stage before commit,
      - commit

<!-- end_slide -->

# automatic rebasing

<!-- jump_to_middle -->
more on this later...

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
<!-- end_slide -->

# [mergiraf](https://mergiraf.org/)
  
resolving conflicts at 60 km/h

- Rust (`*.rs`)
- Go (`*.go`)
- Javascript (`*.js, *.jsx, *.mjs`)
- TypeScript (`*.ts, *.tsx`)
- C/C++ (`*.c, *.h, *.cc, *.hh, *.cpp, *.hpp, *.cxx, *.hxx, *.c++, *.h++, *.mpp, *.cppm, *.ixx, *.tcc`)
- C# (`*.cs`)
- Python (`*.py`)

```bash
jj mergiraf
```

<!-- end_slide -->

![image:width:50%](assets/mergiraf1.png)
<!-- end_slide -->

![image:width:50%](assets/mergiraf2.png)
<!-- end_slide -->

![image:width:50%](assets/mergiraf3.png)
<!-- end_slide -->

# git backend

<!-- jump_to_middle -->
- transparent to others
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

# what I love ❤️

## fluidity of moving around

- try many different approaches, capture them all and compare in VCS (not just in editor undo history)
  - squash
  - rearrange
  - rebase
  - edit

<!-- end_slide -->

# operations log

- undo any operation

<!-- end_slide -->

# demo

- uses [jjui](https://github.com/idursun/jjui)

<!-- end_slide -->

# link dump

Homepage:  <https://www.jj-vcs.dev/latest/>
Github: <https://github.com/jj-vcs/jj>

 [Solving Git's Pain Points with Jujutsu (with Martin von Zweigbergk)](https://www.youtube.com/watch?v=ulJ_Pw8qqsE)
 <https://schpet.com/note/why-i-think-jj-vcs-is-worth-your-time>
 <https://steveklabnik.github.io/jujutsu-tutorial/>
 <https://flames-of-code.netlify.app/blog/my-jj-workflow/>
 [Jujutsu in practice](https://arne.me/blog/jj-in-practice)
 [Jujutsu (jj), a git compatible VCS - Tony Finn](https://tonyfinn.com/blog/jj/)
 <https://etodd.io/2025/10/02/should-i-switch-from-git-to-jujutsu/>
