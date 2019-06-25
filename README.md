# OpenShift Workshop

1. Provision Gogs and Nexus into the `lab-infra` project.
2. Edit `variables.adoc` and set the `guid` variable to the proper value.
3. Deploy the instructions.

	````
	oc new-build . --name=labs --strategy=docker

	oc new-app labs

	oc expose svc/labs
	````
4. The lab instructions will now be deployed at: `http://labs-lab-infra.apps.GUID.openshiftworkshop.com`

You may want to use a URL shortener for the lab instructions URL.