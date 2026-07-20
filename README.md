# GitLab
CSD 380 - Assignemtn 9.2 Team Practice Repo

## Assignment Source

Team Git Practice — simulates using Git in a team environment to prepare for professional development work or the Capstone course.

Tutorial reference: [Git and GitHub for Beginners](https://www.freecodecamp.org/news/git-and-githubfor-beginners/)

### Preparation

- Teams of 3–4 people
- If your group only has 3 people, the Release Manager also plays the role of Developer 3
- Steps must be done in order
- Share GitHub usernames with the Release Manager so everyone can be added as a collaborator
- Roles: **Release Manager**, **Developer 1**, **Developer 2**, **Developer 3**

### Role Assignments for This Group

- **Person1** = Release Manager
- **Person2** = Developer 1
- **Person3** = Developer 2
- **Person4** = Developer 3

## Step-by-Step Instructions

### Phase 1 — Setup

**Person1 (Release Manager)**

1. Create a public GitHub repository named `GitLab`
2. Go to the repository's Settings tab and add Person2, Person3, and Person4 as Collaborators — also add the professor as a Collaborator

**Everyone (Person1, Person2, Person3, Person4)**

1. Accept the collaborator invitation
2. Find the `GitLab` repository, click the green **Code** button, and copy the repo URL
3. Clone the repository to your computer: `git clone <url>`
4. In your terminal, navigate into the cloned `GitLab` folder

### Phase 2 — Foundation Branch

**Person2 (Developer 1)**

1. Create and switch to a new branch: `git checkout -b foundation`
2. Create a file named `index.html` in the `GitLab` folder
3. Add a basic HTML structure to the page (nothing fancy needed yet)
4. Stage the file: `git add index.html`
5. Check status: `git status`
6. Commit: `git commit -m "<your last name>: initial index.html file"`
7. Stop and think: do the other developers have access to this file yet?
8. Push the branch: `git push -u origin foundation`
9. On GitHub, open a pull request comparing `foundation` into `main`

**Person1 (Release Manager)**

1. Open the repository on GitHub and go to **Pull requests**
2. Review Person2's proposed changes
3. If they look good, click **Merge pull request** and confirm the merge

### Phase 3 — Quotes Branch

**Person3 (Developer 2)**

1. Pull the latest changes: `git fetch`
2. Create and switch to a new branch named `quotes`
3. Add an `<h1>` title element to `index.html`
4. Add a `<blockquote>` element with your favorite quote, including the author
5. Create a file named `style.css` (no content needed yet)
6. Stage your changes
7. Commit with a message: `"<your last name>: ..."`
8. Push the `quotes` branch and open a pull request

**Person1 (Release Manager)**

1. Open the repository on GitHub and go to **Pull requests**
2. Review Person3's proposed changes
3. If they look good, merge the `quotes` branch into `master`

### Phase 4 — Styles Branch

**Person4 (Developer 3)**

1. Pull the latest changes
2. Create and switch to a new branch named `styles`
3. Add a couple of basic styles to `style.css` (e.g. a background color, style the quote) and link `style.css` in `index.html`
4. Stage your changes
5. Commit with a message: `"<your last name>: ..."`
6. Decide the quote's author is incorrect and should be "Justin Bieber" — change the author to reflect this
7. Stage your changes
8. Commit with a message: `"<your last name>: ..."`
9. Push the `styles` branch and open a pull request

**Person1 (Release Manager)**

1. Open the repository on GitHub and go to **Pull requests**
2. Review Person4's proposed changes
3. Without noticing the incorrect author, approve and merge the `styles` branch into `master`

### Phase 5 — Hotfix for the Author Error

**Person2 (Developer 1)**

1. The client notices the quote's author is wrong. Person4 is on vacation, so you're asked to fix it
2. Pull the latest changes, and confirm you're on `main` (not a branch): `git status`, `git branch -a`
3. Switch to main: `git checkout main`
4. Create and switch to a new branch named `hotfix1`
5. Correct the author
6. Stage your changes
7. Commit with a message: `"<your last name>: ..."`
8. Do **not** push yet

**Person3 (Developer 2)**

1. Pull the latest changes
2. Create and switch to a new branch named `authorupdate`
3. Your manager asks you to make the author's name all uppercase — make that change
4. Stage your changes
5. Do **not** commit or push yet

**Person2 (Developer 1)**

1. Push the `hotfix1` branch and open a pull request

**Person1 (Release Manager)**

1. Open the repository on GitHub and go to **Pull requests**
2. Review Person2's proposed changes
3. Approve and merge `hotfix1` into `master`

### Phase 6 — Merge Conflict

**Person3 (Developer 2)**

1. Switch to the `master` branch
2. Pull the latest changes
3. Switch back to your existing `authorupdate` branch
4. Run `git merge master` to bring in the new updates
5. Resolve the merge conflict that results
6. Stage your changes
7. Commit with a message: `"<your last name>: ..."`
8. Push the `authorupdate` branch and open a pull request

**Person1 (Release Manager)**

1. Open the repository on GitHub and go to **Pull requests**
2. Review Person3's proposed changes
3. Approve and merge `authorupdate` into `master`

### Phase 7 — The Justin Bieber Incident

**Person4 (Developer 3)**

1. Pull the latest changes
2. Create and switch to a new branch named `hotfix2`
3. Change the author back to "Justin Bieber" (you're certain this time)
4. Stage your changes
5. Commit with a message: `"<your last name>: ..."`
6. Push the `hotfix2` branch and open a pull request

**Person1 (Release Manager)**

1. Open the repository on GitHub and go to **Pull requests**
2. Review Person4's proposed changes
3. This time, leave a comment explaining why it's incorrect and **close the pull request without merging**
4. Let Person4 know there's more to life than Justin Bieber
