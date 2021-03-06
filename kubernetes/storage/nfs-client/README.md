# NFS-client

`PVC` 动态创建 `PV`

NFS 服务端路径 `/exported/path/${namespace}-${pvcName}-${pvName}`

## 准备

* 已经拥有 NFSv4 服务端，这里假设为 `192.168.199.100`，部署时请 **务必** 替换为自己的地址。

## 安装依赖(重要)

```bash
$ sudo apt install -y nfs-common

$ sudo yum install -y nfs-utils
```

## 部署

在 `deploy/deploy.yaml` 将 `192.168.199.100` 替换为自己的 NFS 服务端地址，之后部署：

```bash
$ kubectl apply -f deploy
```

## 参考

* https://github.com/kubernetes-incubator/external-storage/tree/master/nfs-client
* docs/storage/nfs.md
