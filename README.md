# openshift-basic-guide
Guia para workshop basic de Red Hat OpenShift

# Aprovisionamiento de la guia

```
  oc new-project workshop-guide
  oc new-app quay.io/osevg/workshopper --name=guide -e WORKSHOPS_URLS="https://raw.githubusercontent.com/zapata13/openshift-basic-guide/master/_workshop.yml" -e LOG_TO_STDOUT=true
  oc expose svc/guide
  oc create -f https://raw.githubusercontent.com/rmkraus/ocp4-workshop/master/hello_world_template.json -n openshift
```
