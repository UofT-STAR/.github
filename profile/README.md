# UofT STAR

We are the **University of Toronto Student Team for Amateur Rocketry**. Our avionics team works on the hardware and software used in our rockets' flight computers.

## Join the avionics team

Our firmware repository is **[Avionics-Bay](https://github.com/UofT-STAR/Avionics-Bay)**. Start there to explore the Arduino C++ code and PlatformIO configuration.

1. **Connect with the club.** Visit our [joining page](https://utstar.sa.utoronto.ca/join-us.html) for the student Discord community and how to get involved.
2. **Coordinate avionics work with Tymon Cui**, our Director of Avionics ([@ccTymon](https://github.com/ccTymon)). For GitHub access and technical help, share your GitHub username with **Kai ([@KaiYT1](https://github.com/KaiYT1))**.
3. **Accept your UofT-STAR invitation.** Kai can help with the organization invitation and Avionics team membership. Contact him for login, permissions, signing, or GitHub workflow issues.

Organization membership provides Read access by default. Avionics team membership provides Write access to Avionics-Bay. You can read and clone the public repository while waiting for membership; being able to view it does not mean you have permission to push changes.

## Make your first contribution

1. Install **GitHub Desktop**, **VS Code**, and the **PlatformIO IDE** extension for VS Code.
2. Clone [Avionics-Bay](https://github.com/UofT-STAR/Avionics-Bay) with GitHub Desktop and open the repository folder in VS Code.
3. Review `platformio.ini` with a teammate and build the selected program. The current source filter builds `src/test1.cpp`; `src/main.cpp` is excluded.
4. Agree on a small task with Tymon, create a branch, and make your change. A setup-documentation improvement is a useful first task.
5. Check your change and open a pull request describing what you changed and verified. Coordinate avionics review with Tymon and ask Kai for help with commit signing; `main` requires signed commits and PR approval.

**No hardware is needed to clone, compile, or make a documentation contribution.** Arrange a separate sensor-only bench session with a teammate when you are ready to test hardware. Confirm the board, wiring, and bench setup before uploading.

## Check your computer setup

New to Git? Start with GitHub Desktop for cloning and publishing. Install standalone [Git](https://git-scm.com/downloads) for the terminal checks below, plus the PlatformIO IDE extension in VS Code. **GitHub CLI (`gh`) is optional.**

Open your cloned Avionics-Bay folder in VS Code and choose **Terminal > New Terminal**. Run one small block at a time. Copy the commands, not the sample output. **Outputs below are illustrative examples:** your versions, paths, and identity will differ.

### 1. Is Git installed?

**Run:**

```sh
git --version
```

**Example output:**

```text
git version 2.55.0.windows.3
```

If the command is not recognized, install Git and restart VS Code. Continue when a version appears.

### 2. Did you open the right clone?

**Run:**

```sh
git remote -v
```

**Example output:**

```text
origin  https://github.com/UofT-STAR/Avionics-Bay.git (fetch)
origin  https://github.com/UofT-STAR/Avionics-Bay.git (push)
```

Both lines should identify UofT-STAR/Avionics-Bay; SSH URLs are valid too. “Not a git repository” means you should check the folder you opened. Ask for help rather than running `git init`.

### 3. Is your commit identity set?

**Run:**

```sh
git config --get user.name
git config --get user.email
```

**Example output:**

```text
Alex Student
12345678+alexstudent@users.noreply.github.com
```

Expect your own name and a GitHub-associated email. Blank output means the setting is missing; ask Kai to help configure it. These settings identify commits, not your login.

### 4. Is signing configured?

**Run:**

```sh
git config --get commit.gpgsign
git config --get user.signingkey
```

**Example output for SSH signing:**

```text
true
C:/Users/YourName/.ssh/id_ed25519.pub
```

A GPG key ID is also possible. If these settings are blank, coordinate signing setup with Kai. Do not overwrite existing keys. Configuration alone is not proof: your first signed commit must show **Verified** on GitHub after publishing.

### 5. Is PlatformIO available?

**Run in a PlatformIO terminal:**

```sh
pio --version
```

**Example output:**

```text
PlatformIO Core, version 6.2.0
```

If no version appears, finish the extension setup and ask a teammate for help. Next, use the Avionics-Bay setup instructions with a teammate to build the selected program before connecting hardware.

Finally, confirm GitHub Desktop uses the account you gave Kai. Publishing your first feature branch checks Write access; cloning this public repository alone does not. Work on a branch and open a PR rather than pushing directly to `main`.


## Other development repositories

| Repository | Purpose |
| --- | --- |
| [Website](https://github.com/UofT-STAR/Website) | Club website code. |
| [WebsiteV2](https://github.com/UofT-STAR/WebsiteV2) | React and Tailwind website overhaul. |

Website contributors use the **WebsiteDevelopment** team for Write access to those repositories. Coordinate with the club before requesting access to a project.
