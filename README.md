# Ansible create python project

This is ansible-playbook for automatic creating new python project.
It includes:

- Automatic create repository on `github`;
- Clone created repository to your workspace;
- Create files:
  - `.gitignore`
  - `requirements.txt`
  - `README.md`
  - `.env`
- Make initial commit;
- Pushing changes to remote github repo;
- Create virtual environment in the project directory;

## Prerequisites

- `Ubuntu`
- `Python3`
- `ansible`

## How to install

- First, you need to create [Personal access token](https://github.com/settings/tokens) with the following scopes: `repo`, `admin:repo_hook`, `delete_repo`
- Create hidden file `.env` in your home directory with the following content: `GITHUB_TOKEN <access token>`
- Open for edit `vars.yml` and fill the following variables (*note that `project` will clone to the `root_dir`*):

    ```bash
    github_repo_url: https://api.github.com/user/repos
    github_ssh_url: git@github.com:nicko858
    root_dir: /home/nicko/Dropbox
    project: test_project
    ```

## How to run

```bash
ansible-playbook create_python_project.yml
```

## Project Goals

Productivity.
