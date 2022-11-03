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
 <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
 <meta name="Author" content="Made by 'tree'">
 <meta name="GENERATOR" content="$Version: $ tree v2.0.2 (c) 1996 - 2022 by Steve Baker, Thomas Moore, Francesc Rocher, Florian Sesser, Kyosuke Tokoro $">
</head>
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

</p>
	<hr>
	<p class="VERSION">
		 tree v2.0.2 © 1996 - 2022 by Steve Baker and Thomas Moore <br>
		 HTML output hacked and copyleft © 1998 by Francesc Rocher <br>
		 JSON output hacked and copyleft © 2014 by Florian Sesser <br>
		 Charsets / OS/2 support © 2001 by Kyosuke Tokoro
	</p>
</body>
</html>
