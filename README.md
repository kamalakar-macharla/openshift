# openshift
# This is basic pipelinerun with simple basic two tasks which simply displays a Hello World.

git clone 

oc apply -f operator/subscription.yaml	# This takes couple of minutes to install the RedHat openshift pipeline operator.

oc apply -f openshift/build-task.yaml; \
oc apply -f openshift/deploy-task.yaml; \
oc apply -f openshift/pipeline.yaml; \
oc apply -f openshift/pipelinerun.yaml;

tkn pipelinerun logs pipelinerunPipeline still running ...
[build : say-hello] Running the Build

[deploy : say-hello] Doing the deployment
