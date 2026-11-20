# Starfield Version History

Starfield Version History lists every Starfield version from the 2023 review build to today. For each one it shows when it came out, what kind of update it was, and its highlights and links to the patch notes on SteamDB and Bethesda.net.

Open the site: https://taosecurity.github.io/starfield-version-history/

For AI assistants: step-by-step instructions are in [AGENTS.md](AGENTS.md).

## Example

To find out when version 1.14.74 came out, type `1.14.74` in the search box above the tables. The count next to the box changes to "2 versions", and the 2024 table shows two rows:

    Date        Version  Kind   Highlights                              Days since previous
    2024-11-05  1.14.74  Beta   Bug fixes                               36
    2024-11-19  1.14.74  Patch  Free rover Creation, CK gets lip sync   14

The first row is the opt-in Steam beta, and the second is the day everyone got the update. Each row also has links to its patch notes. To see only one kind of update, click **Clear** and type `hotfix` instead, or untick the other kinds in the row of check boxes next to the search box. The page shows the 4 hotfixes.

What's new: see the top of the [live page](https://taosecurity.github.io/starfield-version-history/).

## What the page shows

- A timeline shows every version by kind: launch, major update, patch, hotfix, beta, Creation Kit only and pre-release.
- A table for each year lists the date, version, kind, highlights, days since the previous version and links.
- You can search the versions and highlights, and filter by kind.
- An "Other milestones" section lists events that matter to players and modders but aren't game versions, such as the public opening of the official Creation Kit documentation on 2026-11-19.

## Adding a version

The list lives in one plain file, [`versions.csv`](versions.csv). The page reads it every time it opens, so there is no build step.

1. Open [versions.csv in GitHub's editor](https://github.com/taosecurity/starfield-version-history/edit/main/versions.csv).
2. Copy the last line to a new line and change it.
3. Commit. The page shows the change a minute or two later.

The seven fields are Date, Version, Kind, Highlights, SteamDB, Bethesda (or another article) and Also (one extra link).

- Dates are written year-month-day, like 2026-06-11. The order of lines doesn't matter, because the page sorts them.
- Kind is one of: Launch, Major update, Patch, Hotfix, Beta, Creation Kit only, Pre-release.
- If a field is empty, keep its comma.
- Put text that contains a comma in double quotes: `"Major update with maps, gameplay"`.
- Links start with `https://`.

If a line has a mistake, the page still shows all the other lines and names the bad one in a red box at the top.

## How the list is made

- Richard Bejtlich has kept this list by hand since September 2023. A version appears only after someone adds its line.
- Dates are when each version reached Steam (for betas, when the opt-in beta opened). Xbox and Game Pass sometimes got an update on a different day.
- [SteamDB](https://steamdb.info/app/1716740/patchnotes/) keeps the full list of Steam builds, including ones Bethesda didn't announce.

Found a mistake, such as a wrong date or a missing version? Open an issue: https://github.com/taosecurity/starfield-version-history/issues

## Credits and License

Richard Bejtlich of [Richard Presents Starfield Essentials](https://www.youtube.com/@RichardBejtlich) made this page. I am the developer, and Claude is the programmer. More Starfield tools and references are on the [Richard Presents Development Hub](https://taosecurity.github.io/).

This is an unofficial list, not made or endorsed by Bethesda. Starfield is a trademark of ZeniMax Media.

The page is a single `index.html` that reads `versions.csv` and has no other dependencies. Its code is MIT licensed; see [LICENSE](LICENSE). The version list is a set of facts with links to their sources.
