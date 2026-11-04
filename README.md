# puzzle-rules

Repo for storing puzzle genre rules, variant rules and their combinations, plus additional metadata, assets and example puzzles. It is meant mainly for useful classification, easy access to rules in multiple languages (side-by-side comparison), searching through genre and variant combinations, and access to assets and example puzzles.


## About

This is an attempt to organize genres, variants and their usage, originally for personal use, but shared publicly as well. A lot of inspiration comes from Puzsq and from personal experience with constructing and solving variant (and non-variant) puzzles.

- Genre + variant combinations are listed in **Combinations**, with possible sources where they appeared and example puzzles. A combination can contain multiple genres or variants.
- Some rules might be more specific than on other sites like Puzsq or Eric Fox's Dictionary of Rulesets, to remove possible ambiguities.
- The goal is to include example puzzles for all genres and sometimes for combinations, sometimes in several sizes (for example 3x3, 5x5, 7x7) so you can choose whichever fits better on a page of a PDF.

The first version of the browsing page was made with AI, to quickly see if this way of organizing works.

### Usage

Browse at https://filipbrecher.github.io/puzzle-rules/

Editing is currently possible only with a personal access token. I am considering letting trustworthy people (personal connections) edit as well.

### Language support

English, Japanese and Czech are supported for now, and adding a new language is easy.

- **English**, as the reference language.
- **Japanese**, because most of the rules come from Puzsq and I want to keep their original wording.
- **Czech**, for easier use in Czech tournaments.

Previously, for each tournament I either rewrote the rules, copied them from my personal sheet of puzzles (from Penpa+), searched the official Czech website, or looked through past Czech tournament papers and old LaTeX files. For some tournaments I also needed an English version of the rules, which made it even more annoying.


## Classification Guidelines

These guidelines define what belongs in a genre, a variant or a combination, and how rules are written. They affect how the whole database works, and they may be refined over time.

### Terms

- **Genre**: a puzzle type that is generally acknowledged as a separate genre. It is the base everything else builds on. Each genre has exactly one category.
- **Variant**: a reusable change to the rules of a genre (adding, replacing or, rarely, removing statements). A *general* variant applies to all genres or to one category. A *specific* variant applies to one genre only.
- **Combination**: a set of genres and variants that are used together, for example LITS + Aqre, or a genre + one or more variants or other genres. It can have its own names, examples, notes and, optionally, its own rules.
- **Appearance**: a record of who used a combination, with an author, a source and a note.

### Writing rules

1. **English rules are the reference.** At least the English rules must be correct, precise and unambiguous, because other languages and the combination rules build on them. When the English rules and another language disagree, fix the English rules first.
2. **Other languages** follow their source. The Japanese rules, for example, may keep the Puzsq wording. If two sources differ (one states a rule, the other doesn't), say so in the rules' Note.
3. **One statement per line**, each saying one thing. Statements are written for the base genre only, so they don't mention variants.
4. **Don't repeat common expansions** (see below) in every genre.

### Genres

A genre's rules are the **minimal rules** that the main sources accept as defining the genre. Ask whether removing a statement would make it a different or unsolvable puzzle. If yes, the statement belongs to the genre.

**Expansions that are common for the genre still belong to the genre.** If a genre is usually played with an extra rule or element (for example, walls that block a line from passing), that extra rule is part of the genre's rules and it counts as the base genre, not a variant.

How common it is decides where it goes:

- **Common for this genre:** include it in the genre's rules.
- **Uncommon for this genre but reusable:** make it a variant, and record the genre and variant as a combination.
- **A one-off or specific to one puzzle:** put it in the combination's own rules, or leave it out of the rules if it is a convention (see the common expansions below).

**Implementation conventions count.** If the common implementation of a genre enforces a rule (for example, a line may not cross bold borders) even though some other source leaves it out, treat it as part of the genre and mention the difference in the Note.

### Variants

A variant changes the rules only as far as the result can still be called that genre with a modification, and not a completely different puzzle. It adds rules, replaces parts of the rules or, as an exception, removes rules.

- **Removing rules** should be uncommon, and usually only for one specific genre, not for a whole category.
- **A very small or broad variant is fine.** Many combinations are acceptable, since that is how you can see which genres a variant has been used with.
- A one-off tweak that nobody else uses is not worth a variant. Put it in the combination's own rules.
- **General or specific:** a general variant is attached to one category or to all categories (the default). Use a specific variant only when the change makes sense for one genre alone.
- **Different interpretations** of the same idea for different genres or categories are separate variants. Group them with a shared family (a tag, for example "Grid shape" or "Walls").
- **Grid shapes** (hexagonal, Cairo and so on) are variants. The statements describe how adjacency, rows and directions change.

### Combinations

- A combination should contain **at least one genre**. A variant combined only with other variants, without a genre, is not a puzzle.
- A genre plus a specific variant is a combination too. It is what lets you record appearances for it.
- **How the parts interact** is described in the combination's own rules. For example, if one variant forbids crossing borders and another concerns adjacency, then "cells separated by a border are not considered adjacent" belongs to the combination, not to either variant.
- A combination can have a name of its own, even though most will be unnamed. A name is shown before the list of its parts.
- Several combinations can have the same genres and variants when the rules are interpreted differently. They are kept separate.

### Common expansions

These conventions apply to (almost) all puzzles, so they are **not** written in each genre's rules and are not offered by the page. They are listed here once.

1. **Question marks** in clue cells stand for any valid clue of that puzzle (for example any valid number). Puzzle editors usually assume this even when the rules don't mention it.
2. **Missing cells.** The grid may be missing some cells, which are then not part of the puzzle. It is still a square grid (or another grid), but with some cells removed, so the remaining cells can form any shape: a circle, a grid without its corners, or a grid with holes in the middle. This also applies to hexagonal and other grids.
3. **Black cells** in the grid, when the rules do not mention black cells, are not part of the grid either.
4. **Given features.** Some features of a puzzle may already be given in the problem, even if the rules don't say so. For example, in a region-division puzzle some of the region borders may already be drawn, and in a path puzzle some parts of the path may already be given.
5. **Grid shape.** Rules are written for a square grid by default. If a genre is by default played on another grid (for example hexagonal), say so in its rules or its notes.
6. **Size.** Write the rules for general sizes, unless they are really about a specific size (for example, when the puzzle only works for that size). Sudoku rules, for instance, are for NxN, not only 9x9. If a genre usually uses a particular size, restrict it later with a combination consisting of only that genre, or add it to the genre's Notes.
7. **Shape banks.** Unless the rules say otherwise, any shape bank is allowed. A combination may restrict it (for example Pentominous: polyominoes limited to pentominoes).

### Special cases

**Related genres that other sites list separately.** Ayeheya is Heyawake plus the rule that the shaded cells in every region are 180° rotationally symmetric, so it is recorded as Heyawake + Symmetrical Regions (Shading) because it clearly adds on top of Heyawake. Regional Yajilin is the opposite case: instead of arrow number clues, regions carry counts and the loop does not pass through the number cells. The defining clue of Yajilin would've been replaced, so it stays a separate genre. (The alternative would be to define Yajilin without number clues and treat each clue type as a variant for the Shading category.)

**Genre families (mostly for Walks).** Many puzzles share one frame and differ only by a type, such as Ice Walk, Forest Walk or Morning Walk. Make one base genre (Walk) and a specific variant for each type, grouped by a shared family (for example "walk"). This avoids dozens of near-identical genres, and still lets you combine them into a single puzzle (for example one part Ice Walk and another part Forest Walk), with the combination's rules describing how the variants meet.

**Genres native to another grid (for example Honey Islands).** You can write the rules so that they don't depend on the grid shape, and state the native grid in the Notes. Using another grid is then recorded as a combination with a grid-shape variant. For Honey Islands: "Shade some cells in the grid such that exactly N unshaded regions are formed, containing N cells each. N is given outside the grid.". The Notes say that its native grid is hexagonal, and the original "exactly 6 regions of 6 cells" is the size case described above.

### Quick checklist

1. Is it part of the minimal rules of the genre? Put it in the genre.
2. Is it a common expansion for this genre? Put it in the genre.
3. Is it a universal convention? See the common expansions above.
4. Is it reusable but uncommon for the genre? Make a variant and record a combination.
5. Is it a one-off, or the way parts interact? Put it in the combination's own rules.


## For Contributors

Ask the owner of this repository if anything is unclear.

### Names and statements

When adding or modifying rules, make sure they are correct and consistent across languages. All statements must end in a period, so that copying the raw text of the rules gives correct sentences.

Make sure the translations of puzzle names are correct. You can write multiple names for a puzzle, and add a new one if one is missing. Don't repeat the same name in another language unless you are 100% sure there is no other name for that puzzle in that language.

- "Slitherlink" is the English name, but in Czech it is called "Slitherlink" or "Ploty", so the English "Slitherlink" is not repeated as a separate name.
- "Nurimisaki" is the English name and also the only Czech name, so it is fine to write "Nurimisaki" as the Czech name too.

### Rule sources

The **Source** says where the rules were originally obtained or which source they are based on.

- If the rules come from Puzsq, use the source label specified on Puzsq (for example "Puzsq Rules", "Original" or another source). Don't automatically use "Puzsq Rules" just because the rules were obtained from Puzsq.
- If the rules come from another reference, such as a dictionary, publication, social media post or website, specify that source.
- If the rules are reworded, modified or translated, keep the original source and describe the changes in the **Note**.
- When rules are available in multiple languages, the source refers to the original-language rules, if known, not the translation. Document the translation in the Note.

| Source label | Meaning |
| -------- | ------- |
| Original | Rules taken from the original puzzle publication or the original source in which the rules appeared. |
| Puzsq Rules | Rules obtained from Puzsq, where Puzsq Rules is listed as the source or where there isn't any source listed. |
| Eric Fox's Dictionary of Rulesets | Rules obtained from Eric Fox's Dictionary of Rulesets. |
| Twitter / X | Rules obtained from a Twitter / X post. Include a link to the post where possible. |
| Website name or URL | Rules obtained from the specified website. |
| Dlouhodobá soutěž HALAS | Rules obtained from the HALAS long-term competition. |
| Puzzle Rules | Rules independently written or compiled for this project, without a more specific external source. |

### Rule notes

Use the **Note** to describe any differences between the rules as presented here and those in the original source.

| Note label | Meaning |
| -------- | ------- |
| Reworded | The wording was changed for clarity, readability or consistency with rules for other genres, without changing the meaning. |
| Modified | The rules were changed in some way, resulting in a difference in meaning or interpretation compared to the source. |
| Translated | The rules were translated from the source language into another language. |

### Inventor

The **Inventor** is the person who invented the puzzle genre, not necessarily the person who wrote the rules. If the inventor is unknown, the first known appearance of the genre can be given in the notes instead.


## Progress Tracker

Tracks the sources that were already used to input genres, variants and combinations.

### Puzsq

Continue checking from the publication date of the last ID. I'm not sure if I'll add genres from Instructionless puzzles, as they also usually don't have a name.

- **Genres:** all genres with ID 0 to 0 are done.
- **Genres in Others (non-variant):** all Others with ID 0 to 0 are done.
- **Variants:** all Variant puzzles with ID 0 to 0 are done.

### Tournaments to explore

- [ ] WPC 2026
- [ ] Add more later

### Finished tournaments

- None


## Future Goals

One future goal is to standardize rules so that a general puzzle editor becomes possible: the variability of Penpa+, combined with the easy editing of Puzz.link or Pzprxs and the solving ability of cspuz-solver2. Possibly with the text rules generated automatically from the actual rules that constrain the puzzle.

Main ideas:

- Create or generate puzzles by defining rules on parts of the puzzle and what counts as a solution. Puzzles can then be generated automatically or constructed by hand (the Puzz.link / Pzprxs / Penpa+ approach), with real-time solving, correctness checking, uniqueness checking and so on.
- Support various grids (square, hexagonal and so on).
- Allow custom rules on parts of the puzzle (for example the top left grid is Fillomino, the top right grid is Square Jam, and they are combined with outside clues, or numbers don't repeat in rows but may repeat in columns).
- Offer ready-made "editor presets" for base puzzles (no need to configure all the rules just to make a classic Fillomino puzzle), or combine rules into a completely custom single-use puzzle.
- Support meta-rules (for example assign N rules to N grids, or place 4 grids side by side in a 2x2, possibly rotated, pattern and then solve normally).
- Automatic solving (partial, full or using only basic tricks), probably with SAT, SMT, ILP and similar solvers to make it fast.

I already made a fairly generalised Sudoku problem creator and solver. It can combine multiple sudokus (like a Samurai, but you can define any rule anywhere and even link number hints together to add another layer of hints) and combine variant rules. It generates a random problem with a unique solution, includes over 100 Sudoku variants, and a couple of compatible logic puzzles. It has no front-end editor (only printing of generated puzzles), so everything is written in code, which makes it a bit hard to use. I might make the repo public if there is interest, although the code quality could be better (for example by using design patterns in some places).
