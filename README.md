# Getting Starting with Git and Helpful References

Andrew Weinert's opinion and a curated list of references to help get you started with git, GitHub, and open source development.

- [git-getting-started](#git-getting-started)
  - [My Background and Projects](#my-background-and-projects)
  - [Git vs GitHub](#git-vs-github)
  - [Visual Studio Code and Extensions](#visual-studio-code-and-extensions)
  - [Start with GitHub Guides](#start-with-github-guides)
  - [What are all these files?](#what-are-all-these-files)
    - [gitattributes](#gitattributes)
    - [gitignore](#gitignore)
    - [LICENSE](#license)
      - [Choosing a License](#choosing-a-license)
      - [Name Use](#name-use)
  - [Citation](#citation)

## My Background and Projects

I am one of the leader developers and administrators for two different source projects.

First is the [Low Altitude Disaster Imagery (LADI) Dataset](https://github.com/LADI-Dataset/ladi-overview). The dataset consists of human and machine annotated airborne images collected by the Civil Air Patrol in support of various disaster responses from 2015-2019. The initial release of human annotations focused on operations in response to Atlantic hurricanes (e.g., Hurricane Harvey, Maria, and Florence). A database of imagery metadata is available for all ~500,000 images. Metadata includes information such as date and time information, latitude and longitude coordinates, and camera settings. This project is [included in the Registry of Open Data on AWS](https://registry.opendata.aws/ladi/) and leveraged as part of a [NIST computer vision challenge](https://www-nlpir.nist.gov/projects/tv2020/dsdi.html).

The other technology is the [airspace encounter models](https://github.com/Airspace-Encounter-Models/em-overview). For many aviation safety studies, aircraft behavior is represented using encounter models, which are statistical models of how aircraft behave during close encounters. Encounter models have for decades, and continue currently, to directly support the safe and efficient integration of aircraft systems into the national airspace system. Currently, models focused on the low altitude are in active development to support integration of drone operations where they may encounter other aircraft at low altitude. If you have ever flown a large airplane, the system to help prevent a midair collision between aircraft was partly validated and assesses for safety using one of these models.

## Git vs GitHub

Git and GitHub are two very different things. Git is a version control software that enables programmers to collaboratively develop code. GitHub provides git as service, along with other collaborate features such as access control, bug / issue tracking, continuous integration, wikis, websites hosting ([GitHub Pages](https://pages.github.com/)), and more. According to the [2020 Stack Overflow Survey](https://insights.stackoverflow.com/survey/2020#technology-collaboration-tools-all-respondents), "Of the professional developers who responded to the survey, almost 82% use GitHub as a collaborative tool."

GitHub is not the only git-based or collaborative software service; alternatives include GitLab and BitBucket.

## Visual Studio Code and Extensions

I often use [Visual Studio Code (VSCode)](https://code.visualstudio.com/) when editing READMEs, inspecting text files (CSV, TSV, etc.), querying SQLite databases, minor code edits, and more. VSCode a freeware source-code editor made by Microsoft for Windows, Linux and macOS. According to the [2019 StackOverflow Survey](https://insights.stackoverflow.com/survey/2019#development-environments-and-tools), VSCode was  was ranked the most popular developer environment tool, with 50.7% of 87,317 respondents reporting use.

You can download VSCode from it's website: [VSCode Download](https://code.visualstudio.com/Download)

VSCode is different from Visual Studio. VSCode has support for many popular development features, such as debugging, syntax highlighting, intelligent code completion; while also enabling users to install extensions for additional functionality. Here is a list of some of my favorite VSCode extensions.

- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): Spelling checker for source code
- [Github Markdown Preview](https://marketplace.visualstudio.com/items?itemName=bierner.github-markdown-preview): Changes VS Code's built-in markdown preview to match Github markdown rendering in style and content
- [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter): Jupyter notebook support, interactive programming and computing that supports Intellisense, debugging and more
- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): Markdown linting and style checking for Visual Studio Code
- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one): All you need to write Markdown (keyboard shortcuts, table of contents, auto preview and more)
- [Markdown Preview Github Styling](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles): Changes VS Code's built-in markdown preview to match Github's styling
- [Rainbow CSV](https://marketplace.visualstudio.com/items?itemName=mechatroner.rainbow-csv): Highlight CSV and TSV files, Run SQL-like queries
- [SQLLite](https://marketplace.visualstudio.com/items?itemName=alexcvzz.vscode-sqlite): VSCode extension to explore and query SQLite databases.

To facilitate cross-platform compatibility, I recommend configuring VSCode (or your editor of choice) to use unix style line endings of `LF (\n)`. For three popular text editors, here are instructions on how to enable `LF` endings.

- [Atom: Line Ending Selector Package](https://github.com/atom/atom/tree/master/packages/line-ending-selector)
- [Notepad++: Preferences](https://stackoverflow.com/q/8195839)
- [VS Code: User Preferences](https://stackoverflow.com/q/52404044)

## Start with GitHub Guides

[GitHub Guides](https://guides.github.com/) is an amazing resource and you should start there. I do not want to reinvent the wheel and many of the guides about git are applicable beyond just GitHub. Currently there are ten guides available and I recommend them all. Don't worry though, most are extremely short reads and can be used as handy guides (looking at you [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)).

## What are all these files?

You've read the GitHub Guides and you created your first repository, so what are all these files created by default?

### gitattributes

`.gitattributes` tells git (not GitHub) on how to handle or treat specific file types or define path-specific settings. This is really important for making sure your line endings are cross-platform compability or telling Git which files are binary.

- [A collection of useful .gitattributes templates](https://github.com/alexkaratarakis/gitattributes)
- [Configuring Git to handle line endings](https://docs.github.com/en/github/getting-started-with-github/configuring-git-to-handle-line-endings)
  
### gitignore

`.gitignore` tells git (not GitHub) which files or directories to ignore. Ignored files will not be checked by git for differences nor committed.

- [Ignoring Files](https://docs.github.com/en/github/getting-started-with-github/ignoring-files)
- [A collection of useful .gitignore templates](https://github.com/github/gitignore)

### LICENSE

The [GitHub Doc says it best about licenses](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/licensing-a-repository):
> For your repository to truly be open source, you'll need to license it so that others are free to use, change, and distribute the software.

**I will not use a repository that does not have a license. I cannot legally use any part of a GitHub project, even if it’s public, unless I have been explicitly given the right to do so.**

[The Legal Side of Open Source by Open Source Guides](https://opensource.guide/legal/) is a great resource about the legal implications of open source and why licenses are important.

#### Choosing a License

- [Choose a License.com](https://choosealicense.com/)
- [Open Source Initiative](https://opensource.org/)

#### Name Use

Depending on the license, you may or may not be given rights to the use of a name. For some organization, their name and marks are some of the their most valuable assets. Please be cognizant about name use and an organization's policy. Policies will differ across organizations and here are two examples:

- [Penn State AD07 Use of University Name, Symbols and/or Graphic Devices](https://policy.psu.edu/policies/ad07)
- [Using MIT's Name](https://tlo.mit.edu/use-mits-name-trademark/using-mits-name)

## Citation

*Add DOI Badge onced Archived in Zenodo*
