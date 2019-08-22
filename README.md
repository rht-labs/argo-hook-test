1.  Deploy poolboy
2.  Deploy anarchy-operater
3.  Create secret for Tower
    - name: babylon1-api-creds (defined in anarchyapi resource)
4.  Create AnarchyAPI CR
5.  Create secret for AWS creds
    - name: innolabs (defined in agnosticv)
6.  Create ssh private key secret for agnosticv-operator
    - name: agnosticv-operator-sshkey
7.  Deploy agnosticv-operator
8.  Create AgnosticVRepo CR
    - use spec.sshKey: agnosticv-operator-sshkey
9.  Process the template created by agnosticv-operator
    - oc process agnosticv-operator//innolabs.ocp4.small
