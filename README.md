# Kubernetes Sample

Kubernetesで動くアプリケーションのサンプル集

## 検証環境の構築

**Mac**

[Docker Community Edition for Mac](https://store.docker.com/editions/community/docker-ce-desktop-mac?tab=description)からedge版をダウンロードしてください。
そして、PreferenceからKubernetesを有効にしてください。

### dashboard

Install

```
$ kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/master/src/deploy/recommended/kubernetes-dashboard.yaml
```

```
$ kubectl proxy
```

Access: <http://localhost:8001/ui>

# Author

- [Himenon](https://github.com/Himenon)

# License

MIT

# TODO

- [ ] README