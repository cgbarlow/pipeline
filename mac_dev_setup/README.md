# Mac devpod setup guide

## Pre-requisites
- Mac OS
- Docker Desktop
- DevPod
- DevPod CLI

## Commands
Scripts are located in `Users > [user] > Scripts`, can run from anywhere:

- `devpod-create.sh` - *Creates a new DevPod from templates with interactive provider and IDE selection.*
- `devpod-select.sh` - *Lists existing DevPods with status indicators and allows SSH connection, stopping, or deletion.*

Copy the scripts above to your `Scripts` folder. If you don't know the commands to allow these to run from anywhere, install claude code and ask it to: `allow me to run the scripts in folder x from anywhere`.

***IMPORTANT NOTE:** Ensure you update `TEMPLATES_DIR` and `DEVPODS_DIR` variables in `devpod-create.sh` according to your environment!*

## DevPods location
I keep a folder under `Users > [user] >` called `devpods` where all my devpods live.

I keep my devpod templates in a folder `_templates` in my devpods folder, e.g. `Users > [user] > devpods > _templates > devpod-template1`.

## After creating a new devpod

**Additional DevPod configuration**:

If using `devpod-template1` (which is based on **https://github.com/jedarden/agentists-quickstart/tree/workspace/basic** with the addition of the `config-devpod.sh` script), do the following:

- Run: `./.devcontainer/config-devpod.sh` which automatically sets up the environment accordingly (below provided for info, the script will take care of this):

    ```
    ./.devcontainer/install-tools.sh
    tmux new -t [result of: 'pwd | xargs basename']
    claude -dangerously-skip-permissions
    npx claude-flow@alpha init --force
    curl -sL https://raw.githubusercontent.com/cgbarlow/pipeline/main/claude.md_customisations/yolo_protocols.md >> CLAUDE.md
    ```

**GitHub CLI authentiation**:
- Generate a PAT in GitHub for the specific repo you're working with, ask Claude how to do this if you're not sure how.
- Run claude, and prompt: authenticate to github CLI with the following PAT: then paste it in.
