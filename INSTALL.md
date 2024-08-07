# Developer Environment Setup

A developer environment consists of tools and packages that are required to develop code projects. Usually, developer environments are stored and hosted on your local computer, but there are some situations where a virtual, web-based development environment exists.

## Setting up a Developer Environment
1. Confirm you have a connection to the internet

2. Confirm you have access to a command line interface (CLI) on your local macOS or Linux computer
> Open a command line interface (CLI) window. This may be referred to as 'Terminal' or 'Shell' depending on your computer's operating system
### Windows Users
- If you are using a Windows computer, you will need to install a Linux distribution or use the [Windows Subsystem for Linux (WSL)](https://learn.microsoft.com/en-us/windows/wsl/install) to access a CLI.
```powershell
wsl --install
```

3. Download and install the IC SDK
> The IC SDK is composed of several components that are required for developing on the Internet Computer.

```bash
sh -ci "$(curl -fsSL https://internetcomputer.org/install.sh)"
```
Verify the installation by running the following command:
```bash
dfx --version
```

4. Download and install a code editor
    - [Visual Studio Code](https://code.visualstudio.com/)
    - Setup Visual Studio Code for the Internet Computer by installing the [Motoko Language](https://marketplace.visualstudio.com/items?itemName=dfinity-foundation.vscode-motoko) extension

5. Download and install git

> Many of the DFINITY public repositories are hosted on Github. To clone these repositories, you will need to install git.

### Installation
```bash
sudo apt-get install git
```

6. Download and install Node.js
> Node.js is a JavaScript runtime that is required for developing front-end applications on the Internet Computer.

### Installation
```bash
sudo apt-get install nodejs
```

or use Node Version Manager (nvm)

```bash
    # installs nvm (Node Version Manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

    # download and install Node.js (you may need to restart the terminal)
nvm install 20

    # verifies the right Node.js version is in the environment
node -v

    # verifies the right npm version is in the environment
npm -v
```

7. Assure all packages and tools are updated to the latest release versions
> Having the latest release version assures that you have all of the newest features and bug fixes for each tool to assure for the most seamless developer experience.

