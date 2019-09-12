# OpenShift Workshop

1. Provision Gogs and Nexus into the `lab-infra` project.
2. Edit `variables.adoc` and set the `guid` variable to the proper value.
3. Deploy the instructions.

	````
	oc new-build --name=labs --strategy=docker --binary

	oc start-build labs --from-dir=.

	oc new-app labs

	oc expose svc/labs
	````
4. The lab instructions will now be deployed at: `http://labs-lab-infra.apps.GUID.open.redhat.com`

You may want to use a URL shortener for the lab instructions URL.
