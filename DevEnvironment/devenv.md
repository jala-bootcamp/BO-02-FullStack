# User Configuration

## SSH Keys

Get the machine's IP:

```sh
ip a
```

Copy host SSH key to remote machine:

```sh
ssh-copy-id user@host
```

### Sudoers

Fedora: Add user to group wheel

```sh
gpasswd -a srodriguez wheel
```

Edit sudoers

```sh
sudo visudo
```

### Vim

To move to insert mode press `i`, to leave insert mode press `escape`.

-   `dd` - Delete the whole line
-   `:[Line Number]`: Go to line number
-   `:set number` - To see the line numbers
-   `:wq` or `x!` - Save and quit
-   To copy `v` select and copy with `y`, then paste with `p`.

### Java

Install SDKman after NVM

```sh
curl -s "https://get.sdkman.io" | bash
```

Install Gradle:
```sh
sdk i gradle
```

### NodeJS

Install NVM

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
```

## System configuration

### Development tools

In Fedora
```sh
sudo dnf group install "Development Tools"
```

### Useful apps


#### tmux

Install in Fedora:
```sh
sudo dnf install -y tmux
```

-   To split window horizontally: `ctl + b"`
-   To split window horizontally: `ctl + b%`
-   To maximize pane: `ctl + bz`

### htop

```sh
sudo dnf install -y htop
```

### Jenkins

#### Fedora

```sh
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo dnf upgrade
sudo dnf install jenkins java-devel
```
