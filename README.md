# fruits-chart

TO CREATE AN HELM CHART REPOSITORY :

0) crea un repositopry con un branch gh-pages e ottieni l'url di Github Pages sotto "Settings-> Pages"

1) La struttura della directory del repo deve essere ... 

├── charts
│   └── <nome-del-mio-chart>
│       ├── Chart.yaml
│       ├── templates
│       │   ├── app-cm.yml
│       │   ├── app-pod.yaml
│       │   ├── app-svc.yaml
│       │   ├── ...
│       │   ├── ...
│       │   └── ingress.yaml
│       └── values.yaml
├── index.yaml
└── README.md



2) Utilizzare il comando "helm package charts/<nome-chart>

Verrà generato un archivio <nome_release>-<versione>.tgz

3) helm repo index --url https://davideelliot94.github.io/<nomerepo> .

4) helm repo add fruits-chart https://davideelliot94.github.io/fruits-chart/

5) helm repo update

6) Per vedere cosa c'è nel repo

	helm search fruits-chart

7) per installare 

helm install <nome> fruits-chart/fruits --create-namespace <nome_namespace>


