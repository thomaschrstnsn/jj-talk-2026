---
theme:
  override:
    footer:
      style: template
      left:
        image: ./assets/jj.png
      center: '**Introduction** to <span class="noice">_Jujutsu_</span>'
      right: "{current_slide} / {total_slides}"
      height: 3
    palette:
      classes:
        noice:
          foreground: blue
---

<!-- newlines: 6 -->

![](./assets/jj.png)

<!-- end_slide -->
# what is it?

- [Jujutsu](https://github.com/jj-vcs/jj) is a powerful version control system for software projects. <https://www.jj-vcs.dev/latest/>
- initially developed by Martin von Zweigbergk (employed at Google)
  - now part of the jj-vcs org on github
- used at Google, being rolled out for GA in [the beginning of 2026](https://www.youtube.com/watch?v=v9Ob5yPpC0A)
  - using a different backend (not git) for their monorepo

<!-- end_slide -->

# big ideas

- automatic snapshotting 🎰
- atomatic rebasing ♻️
- anonymous first 🎭
- first class conflicts ⚠️
- git compatible 

<!-- end_slide -->

# automatic snapshotting

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

<!-- end_slide -->

# anonymous first

- branches:
  - name when you are ready to share with others
- changes/commits:
  - describe when you are sure should how you want to "tell your story"

<!-- end_slide -->

# first class conflicts

- conflicts are first class: are stored in your tree and can be solved later, in one go or in many smaller attempts.
  - stored in commits
    - the inputs to the merge
    - cheap to recalculate what a conflict is
      - re-evaluate if it has been resolved
  - jump around and do the work and resolve conflicts when it suits you
    - contrast: in git conflicts are "stop the world" events 😢

<!-- end_slide -->

# aside: [mergiraf](https://mergiraf.org/)

resolving conflicts at 60 km/h

- Rust (`*.rs`)
- Go (`*.go`)
- Javascript (`*.js, *.jsx, *.mjs`)
- TypeScript (`*.ts, *.tsx`)
- C/C++ (`*.c, *.h, *.cc, *.hh, *.cpp, *.hpp, *.cxx, *.hxx, *.c++, *.h++, *.mpp, *.cppm, *.ixx, *.tcc`)
- C# (`*.cs`)
- Python (`*.py`)

<!-- end_slide -->

![mergiraf](assets/mergiraf1.png)
<!-- end_slide -->

![mergiraf2](assets/mergiraf2.png)
<!-- end_slide -->

![mergiraf3](assets/mergiraf3.png)
<!-- end_slide -->

# git backend

- transparent to others
- git is ubiquitous
- git has "ok"-ish UX

<!-- end_slide -->

# Stockholm syndrome?

- who here uses vanilla git in the commandline without any aliases or helper scripts?

> a psychological coping mechanism where hostages or abuse victims develop positive feelings, empathy, or even loyalty toward their captors or abusers

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

 [Solving Git's Pain Points with Jujutsu (with Martin von Zweigbergk)](https://www.youtube.com/watch?v=ulJ_Pw8qqsE)
 <https://schpet.com/note/why-i-think-jj-vcs-is-worth-your-time>
 <https://steveklabnik.github.io/jujutsu-tutorial/>
 <https://flames-of-code.netlify.app/blog/my-jj-workflow/>
 [Jujutsu in practice](https://arne.me/blog/jj-in-practice)
 [Jujutsu (jj), a git compatible VCS - Tony Finn](https://tonyfinn.com/blog/jj/) also mentions potential issues when using with nix flakes
 <https://etodd.io/2025/10/02/should-i-switch-from-git-to-jujutsu/>
