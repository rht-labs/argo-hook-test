1.  Deploy poolboy
2.  Deploy anarchy-operater
3.  Create secret for Tower
    - name: babylon1-api-creds (defined in anarchyapi resource)
4.  Create AnarchyAPI CR
5.  Create secret for AWS creds
    - name: innolabs (defined in agnosticv)
    The secret name for the apac env is innolabs-apac
6.  Create ssh private key secret for agnosticv-operator
    - name: agnosticv-operator-sshkey
7.  Deploy agnosticv-operator
8.  Create AgnosticVRepo CR
    - use spec.sshKey: agnosticv-operator-sshkey
9.  Process the template created by agnosticv-operator
    - oc process agnosticv-operator//innolabs.ocp4.small

**Note**: for now OpenShift 4.1 is supported. OpenShift 4.2 support is dependent on [issue #42](https://gitlab.consulting.redhat.com/rht-labs/labs-sre/documentation/issues/42) resolution.

The folder structure will become the name of the catalog item in the OMP OCP console. There are two items in this repository.
1- The first item is for the innolabs.ocp4.small for the NA clusters
2- The second item is for the apac.ocp4.small for the APAC Clusters.
The difference between them is the AWS credentials(small.yaml), dns zone id(common.yaml) and the ssh key (common.yaml)



