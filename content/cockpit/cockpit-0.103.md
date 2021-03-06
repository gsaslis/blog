Title: Cockpit Ubuntu PPA
Date: 2016-04-20 15:45
Tags: cockpit, linux, technical, kubernetes
Slug: cockpit-0.103
Category: release
Summary: Cockpit releases every week. Here's highlights from 0.103

Cockpit is the [modern Linux admin interface](http://cockpit-project.org/). There's a new release every week. Here are the highlights from this weeks 0.103 release.


### Upload each Release to an Ubuntu PPA

Each weekly release of Cockpit is now uploaded to an Ubuntu PPA. Here's how to make use of it:

    sudo add-apt-repository ppa:cockpit-project/cockpit
    sudo apt-get update
    sudo apt-get install cockpit


### Kubernetes Connection Configuration

When a Kubernetes client wants to access the API of the cluster, it looks for a "kubeconfig" file to tell it how to find the cluster and how to authenticate when accessing the API. The usual location for this file is in the current user's home directory at the ```~/.kube/config``` file path. If that doesn't exist, then usually the cluster isn't available. This applies to both clients like the ```kubectl``` command as well as Cockpit's cluster dashboard.

Cockpit can now prompt for this information, and build this file for you. If it doesn't exist, then there's a helpful "Troubleshoot" button to help get this configuration in place.

<iframe width="853" height="480" src="https://www.youtube.com/embed/WSh7wYhAXrA" frameborder="0" allowfullscreen></iframe>


### Remove jQuery Usage from cockpit.js API

As part of stabilizing the internals of Cockpit, we removed jQuery usage from the cockpit.js file. [The javascript API itself](http://cockpit-project.org/guide/latest/api-base1.html) hasn't changed, but this change helps to help keep a stable API in the future.


### Try it out

Cockpit 0.103 is available now:

 * [For your Linux system](http://cockpit-project.org/running.html)
 * [Source Tarball](https://github.com/cockpit-project/cockpit/releases/tag/0.103)
 * [Fedora 24](https://bodhi.fedoraproject.org/updates/cockpit-0.103-1.fc24)
 * [COPR for Fedora 23, CentOS and RHEL](https://copr.fedoraproject.org/coprs/g/cockpit/cockpit-preview/)

