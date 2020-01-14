[TOC]
#### local kubernetes env
1. 启动 mac docker
2. 运行命令: kubectl proxy
3. kubernetes 启动，dashboard 启动

dashboard url: [kubernetes dashboard](http://localhost:8001/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/#!/overview?namespace=default)
token: eyJhbGciOiJSUzI1NiIsImtpZCI6IiJ9.eyJpc3MiOiJrdWJlcm5ldGVzL3NlcnZpY2VhY2NvdW50Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9uYW1lc3BhY2UiOiJrdWJlLXN5c3RlbSIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VjcmV0Lm5hbWUiOiJkZWZhdWx0LXRva2VuLXA5aDRrIiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9zZXJ2aWNlLWFjY291bnQubmFtZSI6ImRlZmF1bHQiLCJrdWJlcm5ldGVzLmlvL3NlcnZpY2VhY2NvdW50L3NlcnZpY2UtYWNjb3VudC51aWQiOiIwZDY4MjAxYi0zNmRlLTExZWEtOTk5Ny0wMjUwMDAwMDAwMDEiLCJzdWIiOiJzeXN0ZW06c2VydmljZWFjY291bnQ6a3ViZS1zeXN0ZW06ZGVmYXVsdCJ9.Zd-oDqy_3WPNfrqQo81TA8ezF0yBo8G-UAONPCo5dlN8IGtRBGtZJmmRQ-eh1wmsAgRCMHP_tpmfkfflZci4AbCCP24l6Xkrp01WdfWL52ut4wzDXrPwdquIjjWwUKm-Ph6WfSlR1wvyla3OHQoICOrlKSlp5xXDOhO_Vq8PwzCNVvwzm4QzHvF6H7jxr2Pn-w-dvLp4heXjpL0hQPU84RmYAMHXD-9V23ImIkAVmmPCPQadUVv8f0GWgIXHvLVS19VurCwnGsxCptmk37sjmbIdCiAnKFVLiBkIQPdIkSJxEEppPBN7D4DIcQW2CzAeDNYGBMnw0SNiKiYPHY4wRg


#### mumu k8s yaml 1
#### namespace
namespace.yml 创建命名空间
limitRange.yml LimitRange 资源指定限制在某个命名空间上
resourceQuota.yml ResourceQuota 资源指定限制在某个命名空间上

如果在指定了限制之后需要修改，可以使用以下命令，例如
```
kubectl edit resourcequota resourcequota mumu-ns-quota -n mumu-ns
```

#### pod
##### demo
nginx-pod.yml 第一个 pod 定义文件 demo(nginx)
```
# 查看更多信息
kubectl get pods *** -o wide

# 实时查看
kubectl get pods *** -w

# 查看 pod yaml 文件
kubectl get pods *** -o yaml
```

##### liveness
liveness-exec.yml
通过 exec 检测
liveness-httpGet.yml 
通过 http 检测

#### deployment
deployment.yml 第一个 deployment 定义文件



