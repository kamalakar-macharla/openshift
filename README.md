# openshift

$ oc apply -f operator/subscription.yaml	
$ cp ./tasks/hello.yaml ./tasks/build-task.yaml
$ cp ./tasks/hello.yaml ./tasks/deploy-task.yaml

$ vim ./tasks/pipeline.yaml
$ vim ./tasks/pipelinerun.yaml

$oc apply -f tasks/build-task.yaml  
$oc apply -f tasks/deploy-task.yaml		  

$ tkn pipelinerun logs pipelinerun
[build : say-hello] Hello World

[deploy : say-hello] Hello World 
