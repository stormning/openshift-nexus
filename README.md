Nexus on OpenShift
==================

This git repository helps you get up and running quickly with a Sonatype Nexus
installation on OpenShift.

Create an account at http://openshift.readhat.com/

Create a diy application (you can name your application whatever you want)

    rhc app create -a nexus -t diy-1.0

Add this upstream Nexus repo

    cd nexus
    git remote add upstream -m master git://github.com/hongun/openshift-nexus.git
    git pull -s recursive -X theirs upstream master

Then push the repo upstream

    git push

That's it, you can now checkout your Nexus repository at:

    http://nexus-$yournamespace.rhcloud.com/nexus/

