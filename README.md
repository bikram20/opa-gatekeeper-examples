# Sample policies for OPA using Gatekeeper

https://medium.com/@bikramgupta/using-opa-and-gatekeeper-for-admission-control-policies-709c749c76ff

## Every pod/namespace must have a set of labels

Make it mandatory for every pod/namespace to be deployed with a set of labels. 

## Control a specific pod/namespace label

Enable a set of users to assign a specific label to the pods/namespaces in the cluster. Prevent others from using that label.

## How to use

$ git clone <repo>

$ kubectl apply -f  templates/
constrainttemplate.templates.gatekeeper.sh/mandatorylabels configured
constrainttemplate.templates.gatekeeper.sh/privilegedlabels configured
$ kubectl get constrainttemplate
NAME               AGE
mandatorylabels    38m
privilegedlabels   19m
$ 

Then apply one constraint (in the constraints folder) at a time and test the admission control enforcement.


## TBD

- Calico Policy attributes enforcement
- Calico Policy order constraints for different users

 
## References
- Gatekeeper: https://github.com/open-policy-agent/gatekeeper
- OPA: https://www.openpolicyagent.org/docs/latest/policy-language/
- OPA playground: https://www.openpolicyagent.org/
 
