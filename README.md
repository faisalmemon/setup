setup.git
=========
Clone and run this on a new EC2 instance running Ubuntu 12.04.2 LTS to
configure both the machine and your individual development environment as
follows:

```sh
curl https://raw.githubusercontent.com/faisalmemon/setup/master/setup.sh | bash
exit # and then reconnect; easy way to fully reset environment
```

Or alternatively if you want to adjust the setup scripts themselves:
```sh
cd $HOME
sudo apt-get install -y git-core
git clone git@github.com:faisalmemon/setup
```


Hierarchy of git repos
======================

From a new Ubuntu install we have, git repos need to be applied in the sequence:

1.  Repo setup (this repo)
Gets the command line tools.  Then pulls in Repo dotfiles.

2.  Dotfiles.
Automatically pulled in by step (1).  Has faisalmemon customizations; in particular new aliases.

3.  Repo bitstarter.
This is the actual website source code.  It has its own setup script to be run, as well as manual
datafill for API entitlements.


To get ssh github access working
================================

1.  Create a keypair
```sh
ssh-keygen -t rsa
```
Supply the file path
```
/home/ubuntu/.ssh/github_rsa
```

2.  Add the key to the ssh list of keys to try
```sh
eval `ssh-agent -s`
ssh-add /home/ubuntu/.ssh/github_rsa
```

3.  Add the public key github_rsa.pub to the github user account page
