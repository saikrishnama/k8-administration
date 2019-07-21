```
#unix Generate Token: 
kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}')
```
#Windows Generate Token: 
```
:Get the secret users info : >kubectl -n kube-system get secret
c:\helm\ui-useradmin>kubectl -n kube-system get secret
NAME                                             TYPE                                  DATA   AGE
admin-user-token-zsr4q                           kubernetes.io/service-account-token   3      7m38s
attachdetach-controller-token-gjbxp              kubernetes.io/service-account-token   3      27m
bootstrap-signer-token-6z2tc                     kubernetes.io/service-account-token   3      27m
bootstrap-token-4fblsa                           bootstrap.kubernetes.io/token         6      27m
certificate-controller-token-qdpk6               kubernetes.io/service-account-token   3      27m
clusterrole-aggregation-controller-token-phg87   kubernetes.io/service-account-token   3      27m
coredns-token-7bntd                              kubernetes.io/service-account-token   3      27m
cronjob-controller-token-nxdpx                   kubernetes.io/service-account-token   3      27m
daemon-set-controller-token-cxt8p                kubernetes.io/service-account-token   3      27m
default-token-cxmwj                              kubernetes.io/service-account-token   3      26m
deployment-controller-token-szq9g                kubernetes.io/service-account-token   3      27m
disruption-controller-token-2686c                kubernetes.io/service-account-token   3      27m
endpoint-controller-token-bwlgz                  kubernetes.io/service-account-token   3      27m
expand-controller-token-ctlql                    kubernetes.io/service-account-token   3      27m
generic-garbage-collector-token-6p6k8            kubernetes.io/service-account-token   3      27m
horizontal-pod-autoscaler-token-fhwcj            kubernetes.io/service-account-token   3      27m
job-controller-token-2xqj4                       kubernetes.io/service-account-token   3      27m

```

#Filter Scret
```c:\helm\ui-useradmin>kubectl -n kube-system describe secret admin-user-token-zsr4q
Name:         admin-user-token-zsr4q
Namespace:    kube-system
Labels:       <none>
Annotations:  kubernetes.io/service-account.name: admin-user
              kubernetes.io/service-account.uid: a86d924d-626e-472c-8afb-2b14bda6e7e5

Type:  kubernetes.io/service-account-token

Data
====
namespace:  11 bytes
token:      eyJhbGciOiJSUzI1NiIsImtpZCI6IiJ9.eyJpc3MiOiJrdWJlcm5ldGVzL3NlcnZpY2VhY2NvdW50Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9uYW1lc3BhY2UiOiJrdWJlLXN5c3RlbSIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VjcmV0Lm5hbWUiOiJhZG1pbi11c2VyLXRva2VuLXpzcjRxIiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9zZXJ2aWNlLWFjY291bnQubmFtZSI6ImFkbWluLXVzZXIiLCJrdWJlcm5ldGVzLmlvL3NlcnZpY2VhY2NvdW50L3NlcnZpY2UtYWNjb3VudC51aWQiOiJhODZkOTI0ZC02MjZlLTQ3MmMtOGFmYi0yYjE0YmRhNmU3ZTUiLCJzdWIiOiJzeXN0ZW06c2VydmljZWFjY2
91bnQ6a3ViZS1zeXN0ZW06YWRtaW4tdXNlciJ9.hjZXPzdmEJxzRZP0DDrsswd3sCzSUGEFpropHFEzu95XLAsOJVu-LpeQUcCnGj1UCA2rJY9wWrt2p1CjmPkbrNAeec7tTizMpRX600uWhuBllAcukyA4XlEinkYr0dgHdm9XCp6UnbQT1x8nERU12cRwl8J_7IJym5Lu0JdjvRqJ-gy4j7rz_AkRGKPN0mODkzN8Y4uRNlldWFRLH4jkqV2ZgmRtOYKR4iXMZYdUUKikX68gBGbl2lec6d_i-oTSJ6UgQVAJDedMHaGBMVfUmIuz6NR8PecWJInNA1nBUU06tzdu8QR-xKzOmGBtXTfXMhMmAWbBSFCkxXikj25FBQ
ca.crt:     1066 bytes
```

