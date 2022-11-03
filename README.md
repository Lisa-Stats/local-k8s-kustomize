Local K8s deployment with Kind using Kustomize
- Since it is using Kind, have to specify NodePort to be able to call service
- Split up into `base`, `testing`, `staging`
  - testing adds or updates:
    - specific namespace
    - testing- prefix
    - configMap with a testing.env file
  - staging adds or updates:
    - specific namespace
    - staging- prefix
    - configMap with a staging.env file
    - new image
<!DOCTYPE html>
<html>
<head>
<body>
	<h1>Tree Diagram</h1><p>
	├── <a href="/base/">base</a><br>
	│   ├── <a href="/base/creds.txt">creds.txt</a><br>
	│   ├── <a href="/base/dev.env">dev.env</a><br>
	│   ├── <a href="/base/kustomization.yaml">kustomization.yaml</a><br>
	│   ├── <a href="/base/nginx-deployment.yaml">nginx-deployment.yaml</a><br>
	│   └── <a href="/base/nginx-service.yaml">nginx-service.yaml</a><br>
	└── <a href="/overlays/">overlays</a><br>
	&nbsp;&nbsp;&nbsp; ├── <a href="/overlays/staging/">staging</a><br>
	&nbsp;&nbsp;&nbsp; │   ├── <a href="/overlays/staging/kustomization.yaml">kustomization.yaml</a><br>
	&nbsp;&nbsp;&nbsp; │   ├── <a href="/overlays/staging/namespace.yaml">namespace.yaml</a><br>
	&nbsp;&nbsp;&nbsp; │   └── <a href="/overlays/staging/staging.env">staging.env</a><br>
	&nbsp;&nbsp;&nbsp; └── <a href="/overlays/testing/">testing</a><br>
	&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; ├── <a href="/overlays/testing/kustomization.yaml">kustomization.yaml</a><br>
	&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; ├── <a href="/overlays/testing/namespace.yaml">namespace.yaml</a><br>
	&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; └── <a href="/overlays/testing/testing.env">testing.env</a><br>
<br><br><p>
</body>
</html>
