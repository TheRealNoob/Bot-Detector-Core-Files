# How does it work?
The project is broken into 5 separate pieces:
* API
* Database
* Highscores scraper
* Discord/Twitter bot
* Website

The API is the main entry point for the project, with the website being completely separate and standalone - though there are plans to change that.

<!-- https://drive.google.com/file/d/16IO84vE3rJWRclbZAnOIEdKAmx5xAi3I/view?usp=sharing -->
![image](https://user-images.githubusercontent.com/40169115/153727141-0e39c6fe-1fdb-42f4-8019-2552bd127751.png)

# How can i request a new feature or report a bug?
To request a new feature or report a bug you should [open an Issue](https://github.com/orgs/Bot-detector/repositories) on Github.
TODO Create an Issue template for feature requests

[Our discord](https://discord.gg/3AB58CRmYs) is also a viable option, but we prefer to be able to track feature requests, so Github is preferred.  However the Discord is perfect for small questions, or just to chat.

# Can I get involved with development?
Yes!  We have containerized all of our server-side components, so you should be able to be to have a locally runnning instance in less than 10 minutes.  To start development on the RuneLite plugin will take a bit more work.  We could recommend reading the [Runelite guide](https://github.com/runelite/plugin-hub) for getting started developing there.

## requirements

### Windows
* [Docker](https://docs.docker.com/desktop/windows/install/)
* [Git](https://gitforwindows.org)
* We recommend [VSCode](https://code.visualstudio.com), but any IDE will work

Once that is installed, we can begin downloading the code.  Open up Git, cd into the directory you want the project created under, and clone our repos

```sh
git clone https://github.com/Bot-detector/Bot-Detector-Core-Files.git
git clone https://github.com/Bot-detector/bot-detector-mysql.git
git clone https://github.com/Bot-detector/bot-detector-ML.git
git clone https://github.com/Bot-detector/bot-detector-scraper.git
```

Now we just need to start the project

```powershell
cd 'Bot-Detector-Core-Files'
docker-compose up -d
```

## Linux/Unix

These instructions assume you're using `apt` as your package manager - the default with Ubuntu.

* install VSCode - see [Microsoft's documentation](https://code.visualstudio.com/docs/setup/linux)
* install Docker - see [Docker's documentation](https://docs.docker.com/engine/install/ubuntu/)
* install Git - `sudo apt install git` or [Git's documentation](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)


Now we just need to clone the repos and start the project.

```sh
git clone https://github.com/Bot-detector/Bot-Detector-Core-Files.git
git clone https://github.com/Bot-detector/bot-detector-mysql.git
git clone https://github.com/Bot-detector/bot-detector-ML.git
git clone https://github.com/Bot-detector/bot-detector-scraper.git

cd Bot-Detector-Core-Files
docker-compose up -d
```

## Opening Merge Requests
Changes to the project will have to submitted through the process of Merge Requests.  Github has good [documentation](https://docs.github.com/en/get-started/quickstart/contributing-to-projects) outlining this process and how it works, but to summarize it here briefly:
1. Go to our repository and click `Fork`. ![image](https://user-images.githubusercontent.com/40169115/153728214-cd741e4e-b036-4d48-9f47-48c4dc9e99be.png)
2. Clone your newly created repository to your local machine
3. Make your local changes.  Test.  Commit.  And push to your own repo
4. Open a Merge Request


## What contributions are needed?
Features, and bugs are documented as issues in each repository, the project owners, review these, and select some as part of a github project: https://github.com/orgs/Bot-detector/projects.

In the github project you can find the refined github issues that we would like to see implemented.

## Development flow:
1. Make sure you are working in your fork. (copy of the repository)
    - On github desktop, in the top left, you can click "Current repository", select the repository under your name.
2. Create a branch, with a relative name, related to the issue.
    - In github desktop, on the top click "branch" or "current branch" > "new branch".
3. Publish your branch.
    - In github desktop, blue button on the middle of your screen "Publish branch"
4. Create your commits (changes).
    - Small commits, defined scope are preferd.
    - Commit messages are desired.
5. Push your commits.
6. Create a Pull Request (PR)
    - in github desktop, blue button on the middle of your screen "Create Pull Request"
    - this will open your browser, make sure the base repository: "Bot-detector/" and base:"develop"

# What are the coding standards?
During the development process it is desired to write tests.

We use black for linting, in Visual Studio code (vs code), you can right click "format document".

Naming conventions:
- Variable: "snake_case"
- Function: "snake_case"
- Class: "camelCase"
- Table: "camelCase"
- Route: "kebab-case"

We are aware that we were not always consistent with naming, please suggest corrections.

# Who approves my code?
We have automated workflows setup for assigning approvers based on their knowledge in ths project - this person will be the owner of Issue/Merge Request.
