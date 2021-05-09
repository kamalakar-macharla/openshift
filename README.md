# OpenShift
## This is basic pipelinerun with simple basic two tasks which simply displays a echo msg.
```
git clone https://github.com/kamalakar-macharla/openshift.git

oc apply -f operator/subscription.yaml	# This takes couple of minutes to install the RedHat openshift pipeline operator.

oc apply -f ./openshift/build-task.yaml; \
oc apply -f ./openshift/deploy-task.yaml; \
oc apply -f ./openshift/pipeline.yaml; \
oc apply -f ./openshift/pipelinerun.yaml;

tkn pipelinerun logs pipelinerun
```
Pipeline still running ...

[build : say-hello] Running the Build

[deploy : say-hello] Doing the deployment


### If any file edit and re-run
oc delete -f ./openshift/filename.yaml;
oc apply -f ./openshift/filename.yaml
