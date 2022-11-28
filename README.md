# cronjob

## How to use this repo
1. Create a service account like `oc create sa checker-sa -n ${NAMESPACE}`
2. Grant the service account proper access like `oc adm policy add-cluster-role-to-user cluster-reader -z checker-sa`
3. Apply the `oc apply -f script-configmap.yml` to create the configmap, so that the cronjob can mount the script
3. Create the cronjob with the service account
