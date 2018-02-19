# tune-resource


## 主役

- livenessProbe
- readinessProbe
- deployment.spec.container[].resource

## 検証内容

### 通常起動

```bash
# Install
$ helm install --name=rdol ./tune-resource

# Access: http://localhost:5000

# Show log
$ kubectl logs -l release=rdol

# Remove
$ helm delete --purge rdol
```

### スペック不足な起動

#### readinessProbe ON

```bash
# インストール
$ helm install -f poor-values.yaml --name=rdol-poor ./tune-resource
# 値の更新
$ helm upgrade rdol-poor -f poor-values.yaml ./tune-resource
# ログ出力
$ kubectl logs -l release=rdol-poor
# 削除
$ helm delete --purge rdol-poor
```

**Result**

```
Readiness probe failed: Get http://10.1.0.13:5000/: dial tcp 10.1.0.13:5000: getsockopt: connection refused
```

## License

MIT

