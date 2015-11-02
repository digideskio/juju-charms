Trusty Juju Charm for Opencell Billing

# Deploying the charm

    #boostrap Juju environment
    juju bootstrap
    #get logs
    juju debug-log
    # deploy juju gui
    juju deploy juju-gui
    #expose juju-gui for public access
    juju expose juju-gui

# Deploying Opencell Charm

    #deploy backend DB
    juju deploy postgresql
    #deploy Opencell
    git clone https://github.com/opencellsoft/juju-charms.git
    juju deploy --constraints "cpu-cores=2 mem=3G" --repository=/path_to/opencell-charm local:trusty/opencell
    #connect Opencell to the backend DB
    juju add-relation opencell postgresql:db
    juju expose opencell

# Test Opencell Charm

Go to http://<public_ip>:8080 or http://<public_ip>:8080/ (username: meveo.admin, password: meveo.admin) for Admininstration

