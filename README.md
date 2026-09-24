[Download README.md](sandbox:/mnt/data/README.md)

# Linux, Vim, Git, Docker, and Python Survival Guide

Build a practical, beginner-friendly reference for everyday development tasks. This is also an exercise in **Git collaboration**: planning with issues, assigning ownership, working on branches, reviewing contributions, and avoiding merge conflicts.

## 1. Form Your Team

Choose one **project lead** and assign an owner to each topic. Everyone—including the lead—contributes content. Members may own more than one topic.

| Topic  | Suggested Coverage                                                                      | Owner |
| ------ | --------------------------------------------------------------------------------------- | ----- |
| Linux  | Navigation, files, permissions, pipes, processes, and help                              | TBD   |
| Vim    | Modes, navigation, editing, searching, saving, and quitting                             | TBD   |
| Git    | Staging, commits, branches, merging, remotes, undoing changes, and GitHub collaboration | TBD   |
| Docker | Images, containers, Dockerfiles, ports, volumes, and Compose                            | TBD   |
| Python | Running scripts, virtual environments, pip, dependencies, modules, and pytest           | TBD   |

### Project Lead Responsibilities

The lead creates the team repository, invites collaborators, establishes the folder structure, and coordinates assignments and merges. Use `main` as the default branch.

**Only the lead creates or edits common files:** the root `README.md`, root `.gitignore`, shared templates, and repository-wide configuration or workflows. Request changes to these files through an issue assigned to the lead.

Topic owners maintain their own folders, including their topic’s `README.md` and images. The lead maintains the team roster and links in the root README.

```text
README.md           # Lead
.gitignore          # Lead
templates/          # Lead
linux/              # Linux owner
vim/                # Vim owner
git/                # Git owner
docker/             # Docker owner
python/             # Python owner
```

## 2. Build the Guide

**First: create one sample page per topic.** Review the samples together and agree on a format before expanding the guide. The lead records the approved template.

Each page should include:

* **Purpose:** What the command or concept does and when to use it.
* **Examples:** Copyable commands, prerequisites, and expected results.
* **Troubleshooting:** Common mistakes, fixes, and warnings for destructive commands.
* **References:** Official documentation and a link back to the topic index.

**Then: complete the topic.** Use separate pages for related tasks rather than one enormous file. Create an issue for each page or small improvement.

AI assistance is allowed, but **run the examples, verify the explanations, and understand what you submit**. Use disposable practice files or containers when testing destructive commands. Never commit passwords, tokens, or private keys.

## 3. Issue → Branch → Pull Request

Use a shared repository with individual branches for the initial exercise.

1. **Create an issue before editing.** Include a clear goal, one assignee, the exact files involved, and a completion checklist. Check existing issues to avoid duplicate work.
2. **Start from updated `main`.** Create a task branch such as `issue-12-linux-navigation`. Do not do assignment work directly on `main`.
3. **Make focused commits.** Stage only your task’s files and reference the issue: `git commit -m "Add Linux navigation guide #12"`.
4. **Push and open a pull request into `main`.** Describe the change and include `Closes #12`. With default auto-closing enabled, merging into the default branch closes the linked issue. ([GitHub Docs][1])
5. **Review before merging.** Another member checks the instructions, examples, and links. The lead merges approved work; another member must also review the lead’s contributions. Pull requests provide the place to discuss and review those changes. ([GitHub Docs][2])

## 4. Avoid Stepping on Each Other’s Work

* **One owner per task; separate files for parallel work.** Coordinate overlapping changes in the issue before editing.
* **Keep shared files with the lead.** Do not rename another member’s files or reorganize the repository without agreement.
* **Keep branches short-lived.** Submit small pull requests and update from `main` before starting the next task.
* **Inspect your changes before committing.** Avoid unrelated formatting changes. Resolve conflicts with the affected teammate; never force-push shared branches to bypass a problem.

## 5. Optional: Fork-Based Collaboration

For additional practice, agree as a group to use forks. Each member forks the team repository, clones their own fork, works on task branches, and opens pull requests **back to the team repository**. ([GitHub Docs][3])

Keep issues in the team repository. In fork commits, use a full issue reference such as `TEAM_OWNER/REPOSITORY#12`. Keep your fork and local clone updated from the team repository before starting new tasks. ([GitHub Docs][1])

**Forks do not eliminate merge conflicts.** File ownership and communication still apply. Where supported, the lead should protect `main` by requiring pull requests and at least one approval. ([GitHub Docs][4])

**Done means:** accurate content, tested examples, working links, completed issue checklist, peer review, and a merged pull request.

[1]: https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue?utm_source=chatgpt.com "Linking a pull request to an issue"
[2]: https://docs.github.com/articles/using-pull-requests?utm_source=chatgpt.com "Pull requests"
[3]: https://docs.github.com/en/get-started/exploring-projects-on-github/contributing-to-a-project?utm_source=chatgpt.com "Contributing to a project"
[4]: https://docs.github.com/articles/syncing-a-fork?utm_source=chatgpt.com "Syncing a fork"
