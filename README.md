# Install and config
## Assumptions:
- automatic installation without manual editing, unless non-standard location
- usage might require some manual editing of `*.conf` files
- usage only requires location of `user.conf` config file
- dependencies will be installed during the installation process
- script names follow `${PREFIX}-*` pattern

## Steps
- `./.hook` - enable `post-merge` hook
- `./deploy` :
    - `./app/.unlink` - unlink previous version, if exists
    - `./.ungit` - copy to gitignored directory
    - `./.prep` - move files, rename, chmod, chown, etc. if necessary
    - `./.deps` - install dependencies
    - `./.link` - symlink files to system file structure

## Dependencies
- libraries:
- os:
    - `~/.profile.d/*.sh` sourced to set env vars on shell launch
    - follows 'XDG Base Directory Specification'

## Config
- `profile` : required by both install and use
- `app.conf` install only
- `user.conf` use only

# Use: local
## Configure:
- `app.conf`:
## First run and Setup
