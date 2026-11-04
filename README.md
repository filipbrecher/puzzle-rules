# puzzle-rules

Repo for storing puzzle Genre rules, Variant rules, and their Combinations. Plus additional metadata and example puzzles. This is meant mainly for easy access to rules in multiple languages, searching through past Combinations and access to example puzzles.


## Info

I tried to make a simple way to organize the Variants and their usage for personal use, but I will share it publicly as well.
Genre + Variant combinations can be seen in Combinations with possible sources where they appeared or example puzzles. There may be Combinations with multiple Genres or Variants.

Some rules might be more specific than on other sites like Puzsq or Eric Fox's Dictionary of Rulesets to remove possible ambiguities. I also want to include example puzzles for all genres, and sometimes for the combinations (sometimes with multiple example puzzles as well, like a small 3x3, 5x5, 7x7, ... so you can choose whichever fits on some page in a pdf better and stuff like that).

A lot of inspiration comes from Puzsq and personal experience with constructing and solving variant (and non-variant) puzzles.

I wanted to make a quick first page with AI to see if this way of organizing would work.


### Usage

Go to https://filipbrecher.github.io/puzzle-rules where it's accessible for viewing and browsing.

As I said above, I made this primarily for personal use, but I want to share it publicly as well (for browsing through). I am considering allowing other users to also edit, but only to trustworthy individuals (personal connections) using custom access tokens (for now).


## For Contributors

Ask the owner of this repository for further questions or if there is some unclarity.

### Languages and Rule Names and Statements

When adding new rules or modifying existing rules, always make sure that they are correct and somewhat consistent across languages. Make sure that all Statements end in a period so that copying the raw text version of the rules gives correct sentences.

Make sure that translations of puzzle names are correct. You can always write multiple names for a puzzle or always add a new one if it's missing. Don't include the exact same names in other languages unless you are 100% sure that there isn't any other name for that puzzle in that language. (Example: "Slitherlink" is in English, but in Czech it's called "Slitherlink" or "Ploty", so we'd ommit the "Slitherlink" name.) (Another example: "Nurimisaki" is in English, but in Czech it's also "Nurimisaki". There isn't any other used name. It's ok to write "Nurimisaki" as the Czech name in this case.)


### Rule Source Guidelines

**Rule Source** indicates where the rules were originally obtained or which source they are based on.

If the rules are copied from Puzsq, use the source label specified on Puzsq (e.g. "Puzsq Rules", "Original", or another source). Do not automatically use "Puzsq Rules" just because the rules were obtained from Puzsq. If the rules come from another reference, such as a dictionary, publication, social media post, or website, specify that source.

If the rules are reworded, modified, or translated, keep the original source and describe the changes in **Rule Notes**.

When rules are available in multiple languages, the source should refer to the source of the original-language rules, if known, rather than the source of the translation. The translation or other changes should be documented in Rule Notes.

The **Inventor** refers to the person who invented the puzzle genre, not necessarily the person who wrote the rules. If the inventor is unknown, the first known appearance of the genre can be specified in the notes instead.

| Source label | Meaning |
| -------- | ------- |
| Original | Rules taken from the original puzzle publication or the original source in which the rules appeared. |
| Puzsq Rules | Rules obtained from Puzsq, where Puzsq Rules is listed as the source or where there isn't any source listed. |
| Eric Fox's Dictionary of Rulesets | Rules obtained from Eric Fox's Dictionary of Rulesets. |
| Twitter / X | Rules obtained from a Twitter / X post. Include a link to the post where possible. |
| Website name or URL | Rules obtained from the specified website. |
| Dlouhodobá soutěž HALAS | Rules obtained from the HALAS long-term competition. |
| Puzzle Rules | Rules independently written or compiled for this project, without a more specific external source. |


### Rule Notes

Use Rule Notes to describe any differences between the rules as presented on this site and those in the original source.

| Note label | Meaning |
| -------- | ------- |
| Reworded | The wording was changed for clarity, readability, or consistency with rules for other genres, without changing the meaning. |
| Modified | The rules were changed in some way, resulting in a difference in meaning or interpretation compared to the source. |
| Translated | The rules were translated from the source language into another language. |


## Classification Guidelines

These guidelines define what belongs in a genre, a variant or a combination, and how rules are written. They affect how the whole database works, and they may be refined over time.

### Terms

- **Genre**: a puzzle type that is generally acknowledged as a separate genre. It is the base everything else builds on. Each genre has exactly one category.
- **Variant**: a reusable change to the rules of a genre (adding, replacing or, rarely, removing statements). A *general* variant applies to all genres or to one category. A *specific* variant applies to one genre only.
- **Combination**: a set of genres and variants that are used together, for example LITS + Aqre, or a genre + one or more variants or other genres. It can have its own names, examples, notes and, optionally, its own rules.
- **Appearance**: a record of who used a combination, with an author, a source and a note.

### Writing rules

1. **English rules are the reference.** At least the English rules must be correct, precise and unambiguous, because other languages and the combination rules build on them. When the English rules and another language disagree, the English rules are the ones to fix first.
2. **Other languages** follow their source. The Japanese rules, for example, may keep the Puzsq wording. If two sources differ (one states a rule, the other doesn't), say so in the rules' Note.
3. **One statement per line**, each saying one thing. Statements are written for the base genre only, so they don't mention variants.
4. **Don't repeat common expansions** (see below) in every genre.

### Genres

A genre's rules are the **minimal rules** that the main sources accept as defining the genre. Ask whether removing a statement would make it a different or unsolvable puzzle. If yes, the statement belongs to the genre.

**Expansions that are common for the genre still belong to the genre.** If it is usual for a genre to be played with an extra rule or element (for example, walls that block a line from passing), then that extra rule is part of the genre's rules, and it counts as the base genre, not a variant.

How common it is decides where it goes:

- **Common for this genre:** include it in the genre's rules.
- **Uncommon for this genre but reusable:** make it a variant, and record the genre and variant as a combination.
- **A one-off or specific to one puzzle:** put it in the combination's own rules, or leave it out of the rules if it is a convention (see the common expansions below).

**Implementation conventions count.** If the common implementation of a genre enforces a rule (for example, a line may not cross bold borders) even though some other source leaves it out, treat it as part of the genre and mention the difference in the Note.

### Variants

A variant changes the rules only as far as the result can still be called that genre with a modification, and not a completely different puzzle. It adds rules, replaces parts of the rules, or, as an exception, removes rules.

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
6. **Size.** Write the rules for general sizes, unless they are really about a specific size (for example, when the puzzle only works for that size). Sudoku rules, for instance, are for NxN, not only 9x9. If a puzzle needs a particular size, restrict it later with a combination consisting of only that genre, or add it to the genre's Notes.
7. **Shape banks.** Unless the rules say otherwise, any shape bank is allowed. A combination may restrict it (for example Pentominous: polyominoes limited to pentominoes).

### Quick checklist

1. Is it part of the minimal rules of the genre? Put it in the genre.
2. Is it a common expansion for this genre? Put it in the genre.
3. Is it a universal convention? See the common expansions above.
4. Is it reusable but uncommon for the genre? Make a variant and record a combination.
5. Is it a one-off, or the way parts interact? Put it in the combination's own rules.


## Language support

It supports English, Japanese and Czech for now, but it's easy to add a new language. English ... obviously. Japanese because I will use most of the rules from Puzsq so I want to include their original Japanese versions as well. Czech because I want to record Czech versions for easier use in future Czech tournaments 

Previously when making a tournament I either wrote the rules again, went to my personal sheet with all of my puzzles and copied from the rules in Penpa+, searched the official Czech website for puzzles, looked through past Czech tournament papers or through older latex files with those genres. And for some tournaments I needed to make an English version of the pdfs which made it even more annoying.


## Future Goals

One of the future goals is to standardize rules in a way where I could make a general editor (like Penpa+ feature variability combined with Puzzlink's or Pzprxs's easy editing abilities and pzpus-solver2's ability to solve puzzles), but (maybe) with automatically generated text rules from the actual rules that constrain the puzzle.

Main ideas: Editor for puzzle generation or creation - define rules on parts of the puzzle, define what counts as a solution - now you can automatically generate puzzles (puzzle generator) or construct puzzles manually (puzzlink/pzprxs/penpa+ approach) with real-time solving / correctness checking / uniqueness check / etc. Make a puzzle on various grids (square, hex, ...). Can add custom "rules" on parts of the puzzle (eg. top left grid is Fillomino, top right grid is Square Jam, and they are combined with outside clues, or: numbers don't repeat in rows, but may repeat in columns, etc.). Allow to define base puzzles (no need to configure all necessary rules and conditions just to make a classic Skyscrapers puzzle, but choose from a list of already prepared "editor presets") or combine rules to create a completely custom single-use puzzle. Support for meta-rules (eg. assign N rules to N grids, or you have 4 grids and need to place them side-by-side in a 2x2 (possibly rotated) pattern, then solve normally). Automatic puzzle solving (partial / full / only use basic tricks) probably using SAT, SMT, ILP, ... to make it fast.

In the past I already made quite a generalised Sudoku problem creator and solver which allowed to combine multiple sudokus together (something like a Samurai, but image you can define any rule anywhere, and even link number hints together to add another layer of hints) and combine variant rules together. It generated a random problem with a unique solution. I didn't make a frontendeditor for it (only for printing the generated puzzles) for it so everything was written in code and then ran in the page, so it's a bit hard to use. It includes over 100 Sudoku variants. It includes a couple of logic puzzles which were compatible. I might make the repo public if there is interest. Although the code isn't the best quality (Could use design patterns in some places to improve the code quality and readability...).

