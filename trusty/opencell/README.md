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
    juju deploy cs:~opencellsoft/juju-charms/trusty/opencell
    #connect Opencell to the backend DB
    juju add-relation opencell postgresql
    juju expose opencell

# Test Opencell Charm

Go to http://<public_ip>:8080 or http://<public_ip>:8080/ (username: meveo.admin, password: meveo.admin) for Admininstration

