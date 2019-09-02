
## Install New Relic Infrastructure agent

More detailed instructions can be found on [docs.newrelic.com](https://docs.newrelic.com/docs/infrastructure/install-configure-manage-infrastructure/linux-installation/install-infrastructure-linux-using-package-manager)

* Create a configuration file, and add your license key:
`echo "license_key: YOUR_LICENSE_KEY" | sudo tee -a /etc/newrelic-infra.yml`{{copy}}
*Don't forget to update YOUR_LICENSE_KEY*

* Enable New Relic's GPG key:
`curl https://download.newrelic.com/infrastructure_agent/gpg/newrelic-infra.gpg | sudo apt-key add -`{{execute}}

* Update apt repository
`printf "deb [arch=amd64] https://download.newrelic.com/infrastructure_agent/linux/apt bionic main" | sudo tee -a /etc/apt/sources.list.d/newrelic-infra.list`{{execute}}

* Update apt package manager
`sudo apt-get update`{{execute}}

* Install New Relic Infrastructure agent
`sudo apt-get install newrelic-infra -y`{{execute}}