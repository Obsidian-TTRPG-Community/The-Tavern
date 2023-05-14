---
attribution: Craftidore
creation: 2023-05-13
modification: 2023-05-13
type: folder
---

# Contributing

I ([Craftidore](https://github.com/Craftidore/)) made this vault as a showcase of how one might manage knowledge in Obsidian.
Unlike the SRD and Resource vaults in the [Obsidian TTRPG Community](https://github.com/Obsidian-TTRPG-Community), this vault is meant for more original content. 
Notes containing summaries, guides, creative ideas and the like go here, whereas Templates, example Dataview Queries, etc. go elsewhere.
What I'm trying to get at is that this is meant to be used **as an Obsidian vault**.

Because of this, my organizational decisions are designed around someone actively exploring this vault, not grabbing a single piece of information and leaving&mdash;people can do that too, it's just not what the organization is built around.
These goals have led me to make an *opinionated vault*; I have made organizational decisions and note conventions that not everyone will agree with.
That said, I'm more than open to feedback the conventions I've set; 
if you have ideas on how to make things clearer or think some of my current conventions are confusing, please make an [issue on Github](https://github.com/Obsidian-TTRPG-Community/The-Tavern/issues) and I'd love to talk about it.

- [[#Getting Started With Git]]
- [[#Vault Conventions]]

## Vault Conventions

### Folders

- Every folders should have a 'folder note' (file with the same name as the folder) containing info about the folder. Use the [[Folder-Note-Template]] template
- Folders should not be more than 3 levels deep (i.e. folder &rarr; subfolder &rarr; subsubfolder, but no deeper), and any 3rd-level folders need a fair bit of justification as to why they exist. ^ba4587
- Top-level folders are prefixed by a multiple of 10 to enforce order
- Subfolders are prefixed with an incrementing number starting at it's parent folder's number + 1 (i.e. 10's first subfolder is 11, second is 12, etc.)
- Subsubfolders do not need number prefixes,  as they should be a [[#^ba4587|rarity]]

### Notes

#### Filenames

Rules:

- No spaces in filenames&mdash;use dashes instead. Some of use terminals. Also avoid quotes (just omit them).
- Capitalize-Each-Word

Loose Guidelines:

- Notes should usually have prefixes, formatted as `Prefix--File-Name`.
- Prefix should give some indication of what broad category the note is from. This serves both to 
    - give some hint as to the contents of the file when looking at a link to it (If I had never heard of [[Campaign--Eternal-Lies]], I wouldn't know it was a campaign. The `Campaign` prefix gives me some needed context)
    - and to group similar things in a folder together (all the notes on Alexandrian articles in [[20-Bathroom-Library]] are shown together in the file explorer)
- I don't have hard rules on how prefixes need to be determined, just guidelines
- If it's more important that the 'type' of content be known, make that the prefix (i.e. [[Campaign--Eternal-Lies]]).
- If it's more important who the author or organization be associated with the content, especially for sake of grouping files, use that as the prefix ([[Alexandrian--Three-Clue-Rule]] or [[Harper--Lady-Blackbird]])
- No dupe filenames if you can help it.
- In the case of date-based notes (like quests for the [[30-Quest-Board]]), you may use the date in `YYYY-MM-DD` format as the prefix.

#### Frontmatter

All notes should have frontmatter. At the very least, every note should have `attribution`, `creation`, `modification`, and `type` values (included with every Templater template).

|   YAML key   | Meaning                                                                                                                                           |
|:--------------:|:------------------------------------------------------------------------------------------------------------------------------------------------- |
| `attribution`  | Username of the user who wrote the file. This is who should be attributed should this content be reused as-per the CC-BY license this vault uses. |
|   `creation`   | `YYYY-MM-DD` date of note creation                                                                                                                |
| `modification` | `YYYY-MM-DD` date of last note modification                                                                                                       |
| `type` | Type of note (`folder` for folder note, `resource-summary` for most stuff in [[20-Bathroom-Library]], etc.) Should already be filled in based on what template you use. |
|     `link`     | Link to resource the note is about.                                                                                                               |
|    `author`    | Author of the resource the note is about.                                                                                                         |
| `content-type` | Type of content this note is about (i.e. `video`, `article`, `book`, `podcast`)                                                                   |
|     `date`     | Date the resource this note is about was published/released/etc. Guess if you have to.                                                            |

#### Contents

- Each file should have an H1 header, even if that H1 header is just `` `=this.file.name` ``.
- No more than 1 H1 header per note
- Most files should have an h2 header called "Related" at the end, listing what other things relate to this note and why
- Assume that the note is being viewed in reading mode (so stuff like `&mdash;` are fine).
- Use html escape codes for non-ascii characters when possible
- Always use a Templater template, even if you just use the [[Generic-Template]].
- **Strict Line Breaks is on**. Be sure to include 2 linebreaks between paragraphs, and 2 spaces at the end of lines when you want a linebreak afterwards.
- With strict line breaks on, I tend to put each sentence on it's own line. I won't make you do this if you don't want to, just mentioning it.

## Getting Started With Git

This guide assumes you've used git before. If you haven't, refer to the git contribution guide for the TTRPG share repo (it doesn't exist yet, just @ me in the Obsidian discord until then, and I'll walk you through it).

1. Fork vault on github
2. Clone vault locally
3. Duplicate the `.obsidian` folder inside the vault, and rename it to `.yourGithubUsername`
4. At the bottom of the `.gitignore` file, add `.yourGithubUsername/` on it's own line.
5. Open Obsidian, and in Settings → About, set your configuration folder to `.yourGithubUsername`
6. Go install the plugins listed in the [[00-Behind-The-Bar/02-Attachments/README|README]] (the settings should already be setup from the copied config folder)

This lets you use your own hotkeys/settings/etc. without accidentally modifying the vault settings.

Before PRing, be sure to check over any of your files in Reading Mode with the `.obsidian` folder's config instead of your custom config.
