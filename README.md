# Sales-App - Quick Start Guide
Welcome to your new sales app template! This template is built with Reflex and integrates OpenAI for enhanced AI-driven features.

## Setup Instructions

### 1. Basic setup

```shell
## Update and Upgrade
sudo apt update && sudo apt upgrade -y
## Install the virtualenv tool and unzip
sudo apt install python3.12-venv unzip

## Install the `bun` package manager for later use with Reflex
## If you have Node.js v20+ installed, this is not neccessary!
curl -fsSL https://bun.sh/install | bash
## activate the .bashrc to make sure `bun` is accessible
source ~/.bashrc
```

### 2. Create .venv and give a go

```shell
## Make project directory
mkdir reflex-nba-dash
cd reflex-nba-dash
## create a venv named as '.venv'
python3 -m venv .venv
## activate it
source .venv/bin/activate
## list the modules in the .venv (only 'pip' itself)
pip list
## Optuioally upgrade pip
pip install --upgrade pip

## Ensure the python3 and pip are from the .venv, 
## if output is like "/usr/bin/", then remake the .venv
which python3
which pip
```

Note: <font color="red">The ops below are in the Virtual Environment.</font>

### 3. Install reflex module

```shell
pip install reflex==0.6.4
```
### 4. Install the template

```shell
reflex init --template sales_app
```

### 5. Install Dependencies

```shell
pip install -r requirements.txt
```
### 6. Set Your OpenAI API Key
To utilize OpenAI in this template, you need to set your __OPEN_AI_KEY__ environment variable. Here’s how you can set it based on your operating system's terminal or setup in `~/.bashrc` (in Linux) or `~/.zshrc` (in macOS).

__On Linux / macOS (Terminal)__:

```shell
export OPEN_AI_KEY=your-openai-api-key
```

__On Windows (Command Prompt)__:

```shell
set OPEN_AI_KEY=your-openai-api-key
```

__On Windows (PowerShell)__:

```shell
$env:OPEN_AI_KEY="your-openai-api-key"
```

### 7. Run the App
After setting up your environment variable, you can start the app:

```shell
reflex run
```
This will launch the app locally and you can interact with it in your browser. 

Eventually, you will be presented with:

> App running at: http://localhost:3000 
>
> Backend running at: http://0.0.0.0:8000

### Notes
- Make sure you have your OpenAI API key. If you don’t have one, you can get it by signing up at [OpenAI](https://openai.com/api/).
- You can permanently set the environment variable in your shell configuration (e.g., `.bashrc` or `.zshrc` for Linux/macOS) to avoid setting it every time.
Enjoy building with Reflex and OpenAI!



## Push the Project to GitHub

1. Create a empty repository on your GitHub space, named as, say `nba-data-dash`.

2. Edit the `.gitignore` file to exclude the `venv` folder.

3. Commit and Push to the repo:

   ```shell
   ## Add data files in
   git add .
   ## Commit
   git commit -m "sales-app"
   ## channel it to master - sorry not a fan of main
   git branch -M master
   ## conenct to remote repo
   git remote add origin https://github.com/marcuszou/reflex-sales-app.git
   ## Push the project files
   git push -u origin master
   ```

   

## License

MIT
