# Ever Projects Commit and Pull Request Guidelines

To ensure a clean, consistent, and professional Git history, all team members must follow these guidelines when writing **commit messages** and creating **pull requests**.

This guide will help everyone in the team — from beginners to advanced developers — to contribute in a clean and efficient way.

## 1. Commit Message Guidelines

### 1.1. Commit Structure

Each commit message must follow **this structure**:

```bash
type(category): [module] short description
```

- **type**: The type of change (`feat`, `fix`, `docs`, etc.) you did
- **category**: The main part of the project concerned you worked on (`web`, `api`, `mobile`, `desktop`, etc.).
- **[module]**: The specific feature, module, or task inside the project you worked on.
- **short description**: A brief but meaningful explanation of the change you did. Start with a verb in infinitive form (e.g., "add", "fix", "improve", refactor, …), **no period at the end**.

Example:

```bash
feat(web): [authentication] add login route
fix(api): [tasks] resolve issue with task creation
```

### 1.2. Types of Commits

| Type | Purpose |
| --- | --- |
| `feat` | Adding a new feature |
| `fix` | Fixing a bug |
| `docs` | Documentation changes only |
| `style` | Code style changes (formatting, indentation, etc.) |
| `refactor` | Code refactoring without changing behavior |
| `test` | Adding or updating tests |
| `chore` | Maintenance tasks (configs, non-production code) |
| `build` | Changes related to build system or dependencies |
| `ci` | Changes to CI/CD configuration or pipelines |
| `perf` | Code changes that improve performance |
| `revert` | Reverting a previous commit |
| `deps` | Updating dependencies |

### 1.3. Examples of Good Commit Messages

### ➔ Adding a feature

```bash
feat(web): [authentication] add login route
```

### ➔ Fixing a bug

```bash
fix(api): [tasks] resolve task creation issue
```

### ➔ Updating documentation

```bash
docs(mobile): [readme] update installation instructions
```

### ➔ Changing code style

```bash
style(web): [fonts] adjust font formatting
```

### ➔ Refactoring code

```bash
refactor(api): [performance] optimize database queries
```

### ➔ Updating tests

```bash
test(web): [authentication] add tests for login functionality
```

### ➔ Maintenance / Chore

```bash
chore(mobile): [dependencies] update third-party libraries
```

### ➔ Updating build system

```bash
build(web): [webpack] upgrade to version 5.0.0
```

### ➔ CI/CD configuration change

```bash
ci: [github-actions] update workflow configuration
```

### ➔ Improving performance

```bash
perf(api): [caching] implement result caching
```

### ➔ Reverting a previous commit

```bash
revert(web): revert "feat(authentication): add login route"
```

### ➔ Updating dependencies

```bash
deps: [all] update to latest version of dependencies
```

## 2. Pull Request Guidelines

### 2.1. Pull Request Title Structure

Each Pull Request title must follow **this structure**, based on @evereq’s recommendation:

```bash
[Type]-APP-#Issue Short description
```

- **[Type]**: Written in brackets and in capital letters (`[Feat]`, `[Fix]`, `[Docs]`, etc.).
- **APP**: The main part of the project affected (`WEB`, `API`, `MOBILE`, `DESKTOP`, etc.).
- **#Issue**: The GitHub issue number related to the PR.
- **Short description**: A short and clear sentence explaining the purpose.

**Example:**

```bash
[Feat]-WEB-#3736 add login form validation
[Fix]-API-#3750 fix user profile timezone issue
```

**Important:**

- Always reference the GitHub Issue number (`#Issue`) if possible.
- Write the short description in lowercase, starting with a verb in infinitive form.
- Be clear and concise — no need for long sentences.

### 2.2. Pull Request Description

The Pull Request description must include:

- **What has been done**: List or explain briefly what you have changed or added.
- **Related issues**: Mention the issue(s) using keywords like `Closes #3736` or `Fixes #3750` (even if already in the title).
- **How to test**: Explain how a reviewer can test your changes.
- **Additional notes** (optional): Anything important like migrations, impacts, or deployment steps.

**Example:**

```markdown
### What was done
- Added validation to the login form.
- Display error messages below inputs.

### Related issue
Closes #3736

### How to test
- Go to `/login` page.
- Try submitting empty fields, check validation errors appear.
- Check no console errors.

### Additional notes
- None.
```

## 3. Best Practices (Commits + PRs)

### Commit Best Practices

- **Commit often**: Keep commits small and focused on one task.
- **Use clear and actionable verbs**: Use words like "add", "fix", "improve", "refactor", "remove".
- **No WIP (Work In Progress)** commits on the main branch.
- **No vague messages** like "update", "fix bug", or "changes".

```bash
feat(web): [dashboard] implement daily plan view
fix(api): [auth] correct token expiration validation
```

### Pull Request Best Practices

- **Keep your PRs small**: Focus on one feature or one problem per PR.
- **Always update your branch** before opening a PR:

```bash
git fetch origin
git rebase origin/develop
```

- **Request reviews** from the right team members.
- **Check the CI/CD pipeline**: Make sure all checks pass before requesting a merge.
- **Write a clean and complete description**.
- **Link issues correctly** in both the title and the description.

## 4. Quick Summary Table

| Action | Format | Example |
| --- | --- | --- |
| **Commit** | `type(category): [module] short description` | `feat(web): [authentication] add login form` |
| **Pull Request Title** | `[Type]-APP-#Issue Short description` | `[Fix]-API-#3750 fix timezone issue` |
| **PR Description** | Clear summary + Related issue + How to test + Notes | As shown above |

By following these rules:

- You **help the whole team** work faster and more efficiently.
- You **make Git history easier to read** and to search.
- You **make it easier** to generate automatic changelogs and release notes.
- You **show professionalism** in open-source or internal company projects.

**Thank you for helping keep our project clean, professional, and scalable !**

### References and Further Reading

- [Conventional Commits Specification](https://medium.com/r/?url=https%3A%2F%2Fwww.conventionalcommits.org%2F)
- [Clean Code by Robert C. Martin](https://medium.com/r/?url=https%3A%2F%2Fwww.goodreads.com%2Fbook%2Fshow%2F3735293-clean-code)
- [How to Make a Git Commit Message Good](https://medium.com/r/?url=https%3A%2F%2Fcbea.ms%2Fgit-commit%2F)
- [GitHub Documentation on Closing Issues via PRs](https://medium.com/r/?url=https%3A%2F%2Fdocs.github.com%2Fen%2Fissues%2Ftracking-your-work-with-issues%2Flinking-a-pull-request-to-an-issue)
