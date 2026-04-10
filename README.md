# UChicago Notes

Selected lecture notes of varying degrees of polish.

## Table of Contents

- [Courses](#courses)
  - [Spring 2026](#spring-2026)
  - [Winter 2026](#winter-2026)
  - [Autumn 2025](#autumn-2025)
- [Features of Notes](#features-of-notes)
- [LiveTeXing Setup](#livetexing-setup)

## Courses

<details>
<summary>Show courses</summary>

### Spring 2026

ECMA 30760: Introduction to Economic Design

ECMA 31150: Econometric Methods for Macroeconomics

ECON 21031: Econometrics II -- Honors

ECON 24050: Labor Economics and Public Policy

### Winter 2026

[ECON 21030](https://github.com/kuomarcus22/UChicago-Notes/tree/main/ECON21030/Lecture%20Notes): Econometrics -- Honors

[ECMA 30800](https://github.com/kuomarcus22/UChicago-Notes/tree/main/ECMA30800/Lecture%20Notes): Theory of Auctions

[STAT 38100](https://github.com/kuomarcus22/UChicago-Notes/tree/main/STAT38100/Lecture%20Notes): Measure-Theoretic Probability I (the most refined notes set)

[STAT 37400](https://github.com/kuomarcus22/UChicago-Notes/tree/main/STAT37400/Lecture%20Notes): Nonparametric Inference

### Autumn 2025

Worse quality than Winter 2026.

[ECMA 33210](https://github.com/kuomarcus22/UChicago-Notes/tree/main/ECMA33210/Lecture%20Notes): Advanced Topics in Macroeconomics (not a superset of content in slides)

[MATH 23500](https://github.com/kuomarcus22/UChicago-Notes/tree/main/MATH23500/Lecture%20Notes): Markov Chains, Martingales, and Brownian Motion

[MATH 27300](https://github.com/kuomarcus22/UChicago-Notes/tree/main/MATH27300/Lecture%20Notes): Basic Theory of Ordinary Differential Equations

[STAT 24410](https://github.com/kuomarcus22/UChicago-Notes/tree/main/STAT24410/Lecture%20Notes): Statistical Theory and Methods 1a

</details>


## Features of Notes

To give credit: the format of the notes from Winter 2026 and on was heavily inspired by a set of course notes by Alexander Torgovitsky.

Some nice features of my notes I would like you to notice:

- Often in class, a theorem is presented, then a necessary lemma is introduced and proved before returning to the theorem. This provides a challenge to my automatic proof numbering system, which searches back for the immediately preceding counter to use in "Proof of Theorem A.B.C." To get around this without changing the theorem--lemma--lemma--theorem sandwich (good sandwiches have the bread on the outside for a reason), I am able to manually override the "name" of proofs.

- The QED symbols (from the fontawesome5 package) differ based on what is being proved. Proofs of *lemmas* end with an unlocked lock, as *lemma* and *lock* start with the letter L, and *lemmas* un*lock* a tool for later use. Theorem, proposition, and corollary proofs end with a Kiwi bird symbol. Examples (note: not example proofs!) end with a frog symbol because there were no good fontawesome5 symbols that started with the letter E.

- Theorems and propositions are in a medium-toned green, while lemmas and corollaries are in a lighter green. This is because the first two are usually "main" results and should stand out more. Definitions are yellow, examples are red-orange-brown, and assumptions are brown-red-orange. These rounded out a (hopefully) harmonious color palette. Proofs and body text are not in a color box environment because if everything is highlighted, nothing is highlighted.

- I try to use footnotes and boxed margin notes intentionally: footnotes are for when I need the comment to point to a specific part (often word) in the text or for when the comment is *very* unrelated, while margin notes are preferred (to avoid too much pointless white space) and used when ambiguity of the anchoring point is fine. I am better about this in later courses.

![Theorem and lemma screenshot](assets/thm-lemma-readme.png)

## LiveTeXing Setup

These notes are typeset in real time during lectures and minimally cleaned up afterwards (usually as I go through them when studying for midterms/finals).[^1]

I use Neovim with VimTeX, Skim, and UltiSnips. Snippets are what allow me to LiveTeX.

The snippets started from Gilles Castel's [guide](https://castel.dev/post/lecture-notes-1/) on LiveTeXing, which seems to have helped many people.[^2] The full snippet file is at `shared/snippets/tex.snippets`. It's a bit messy and idiosyncratic; I would recommend starting with Castel's snippets and building your own as you see fit.

---

[^1]: Starting in Spring 2026, some lecture notes are built around the course slides fed into an LLM, where I add onto the slide content during class. Why do this instead of annotating the slides? It's because I'm lazy, and want everything in one place, in one format --- I don't want to read handwriting (even my own), and I would prefer to digest content from lecture slides in a textbook style consistent across courses. I can also edit and rephrase the content of the slides if an explanation doesn't click with me. The LLM does give a benefit, since lectures from slides (as opposed to those based on board work) often go too fast to copy everything important *and* process all the spoken information. I'm still fine-tuning the agent skills used to convert slides into notes skeletons.

[^2]: If you follow his guide, you will notice he uses Zathura as a PDF viewer. If you're on a Mac, save yourself the failed troubleshooting I went through and use a different viewer like Skim. (Skim is particularly nice because it's quick and auto-refreshes PDFs when they are rewritten.)
