# basic-webserver-apache-gcp
Running a basic Apache web server on Google Cloud Platform

Created by following the instructions here https://cloud.google.com/compute/docs/tutorials/basic-webserver-apache

----

## Set up a new Linux instance.
### [Quickstart using a Linux VM](https://cloud.google.com/compute/docs/quickstart-linux)
  1. New project called **Linux-Apache** (ID boxwood-theory-323621)
      1. Enable billing
      1. Enable [Compute Engine API](https://console.cloud.google.com/apis/library/compute.googleapis.com?project=linux-apache-323621&folder=&organizationId=)
      1. New VM instance ***apache-linux1**
      1. In the Boot disk section, click Change to begin configuring your boot disk.
          - On the Public images tab, choose Ubuntu 20.04 LTS Minimal.
            - Balanced persisted disk: 10 GB
          - In the Firewall section, select Allow HTTP and HTTPS traffic.
          - Custom hostname **thisismycustom.hostname**
          - e2-micro (2 vCPUs, 1 GB memory)
      1. Instance Schedule called **minimal** - between 6-8 pm daily only
  1. Connect to the new Linux instance.
      1. Use the SSH button in the Google Cloud Console to connect
      2. Run command `sudo apt update && sudo apt -y install apache2` to install apache server
      3. Make a copy of the default index file `sudo cp index.html index.html.orig`
  1. Navigate to http://104.154.53.95/ to see the page

----
next up:
## [Build a to-do app with MongoDB](https://console.cloud.google.com/getting-started?walkthrough_tutorial_id=compute_quickstart)
