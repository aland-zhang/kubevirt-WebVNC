# virtVNC

[noVNC](https://github.com/novnc/noVNC) for [kubevirt](https://github.com/kubevirt/kubevirt)

kubernetes > 1.24

## Deploy

```bash
kubectl apply -f https://raw.githubusercontent.com/ES-Yukun/kubevirt-WebVNC/main/webvnc.yaml
```

## Usage

1. Get node port of ```virtvnc``` service
```bash
kubectl get svc -n kubevirt virtvnc
```
2. Visit following url in browser
```
http://NODEIP:NODEPORT/
```

If you want manager virtual machines in other namespace, you can specify namespace using query param namespace like following:
```
http://NODEIP:NODEPORT/?namespace=test
```
![virtVNC](https://github.com/wavezhang/virtVNC/blob/master/virtvnc.gif?raw=true)
