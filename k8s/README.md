#### liujingyi
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



