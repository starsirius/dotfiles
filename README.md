# Dotfiles

## Vim

This uses Vim's native package system (introduced in Vim 8) to manage plugins. 

### Installation

1. Fork the repository to your GitHub account

1. Clone your fork:

    ```sh
    git clone https://github.com/your-github-username/dotfiles.git
    ```

1. Symlink your home .vim directory to the vim directory of the repository

    ```sh
    ln -s /path/to/dotfiles/vim ~/.vim
    ```

1. Initialize and fetch all submodules

    ```sh
    cd  /path/to/dotfiles
    git submodule init
    git submodule update
    ```

### Update

- Update all plugins to the latest master branch

    ```sh
    git submodule update --remote
    ```

- Update a specific plugin to the laster master branch

    ```sh
    git submodule update --remote vim/pack/vim-javascript
    ```

- Delete a specific plugin (see `git help submodules` for more details)

    ```sh
    # git rm && git commit
    git rm vim/pack/vim-javascript/start/vim-javascript
    git commit
    # Remove the entry in .git/config
    vim .git/config
    # Remove the git directory under .git/modules
    rm -rf .git/modules/vim/pack/vim-javascript
    ```
