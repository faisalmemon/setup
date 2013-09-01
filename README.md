setup.git
=========
Clone and run this on a new EC2 instance running Ubuntu 12.04.2 LTS to
configure both the machine and your individual development environment as
follows:

```sh
curl https://raw.github.com/startup-class/setup/master/setup.sh | bash
exit # and then reconnect; easy way to fully reset environment
```

Or alternatively if you want to adjust the setup scripts themselves:
```sh
cd $HOME
sudo apt-get install -y git-core
git clone git@github.com:faisalmemon/setup
```
