# Getting Started

## Prerequisites

- Install kOS Studio
- Configure an image with a backend
- Configure port mapping

Open kOS Studio and show explore the configured and running `tutorial` image

## Description

### Download and install VS Code

<a target="_blank" href="https://code.visualstudio.com/Download" >Download VS Code here</a>


### Install NodeJS using nvm

Go to the NVM website to get the download script

<a target="_blank" href="https://github.com/nvm-sh/nvm" >Visit the NVM Github Page</a>

Run the install script using curl or wget

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

install the latest Node LTS release (lts/hydrogen)

```
nvm install lts/hydrogen
```

Use the installed node version:

```
nvm use lts/hydrogen
```

Set the default node version to be used in all terminal windows:

```
nvm alias default lts/hydrogen
```

### Setup npm to use GitHub Access Tokens

<a target="_blank" href="https://www.kosdev.com/v0.1-SNAPSHOT/page/100152/access-tokens">Latest instructions to install GitHub Access Tokens</a>

<a target="_blank" href="https://www.kosdev.com/v0.1-SNAPSHOT/page/100152/access-tokens#for-react-developers">Configure NPM to use Access Tokens</a>


### Install the kOS UI CLI

Install the CLI used to scaffold out the development environment

```
npm install -g @kosdev-code/kos-ui-cli@snapshot
```

### Create a new UI Development Environment

```
kosui project --projectName dispenser-ui --modelProjectName dispenser-model
```

CD into the new project

```
cd dispenser-ui
```

Open the project in VS Code

```
code .
```

### Start using the integrated terminal

Open the terminal using either the Command Palette:

Mac - Command ⌘ + Shift ⇧ + P

Windows - Ctrl + Shift + P

and select

```
Terminal: Create New Terminal
```

Alternately, just use the built in keyboard shortcut:

Mac - Control ⌃ + `

Windows - Ctrl + `

### Install all the node modules for the generated project

First thing is to install all of the node modules for the project using NPM.

```
npm install
```

### Explore the scaffolded project

Add the recommended VS code plugins

#### Preconfigured dependencies

open the `package.json` file and explore the built int dependencies including

- kos-ui-sdk
- kos-dispense-sdk

#### Integrated environment management

Open the `.env.local` file and confirm that the Java command and kOS Studio install path is correct

### NX Monorepo

Open the `apps` folder and look in the dispenser-ui application

Open the `apps/dispenser-ui/src/app/app.tsx` file to observe the `KosCoreContextProvider`.

Open the `apps/dispenser-ui/src/registration.ts` file to explore the kOS Model registration

Open the `apps/dispenser-ui/.env` file to look at available environment variables for the specific application

open the `libs/models/dispenser-model/src/lib` folder and explore the `dispenser-model.ts`

#### Explore the NX Console

1. Run the build for the dispenser-ui project
1. Run the same command using the CLI as provided in the NX Console terminal
1. Run the serve command for the dispenser-ui project
1. [Open](http://localhost:4200) the link that appears in the integrated terminal.
1. Run the kab command for the dispenser-ui project
