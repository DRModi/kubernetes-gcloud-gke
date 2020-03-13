# Kubernetes Crash Course for Java Developers on Google Cloud

## Learn Kubernetes and Docker with Google Kubernetes Engine deploying Spring Boot Microservices

Look No Further!

## First Commands

```
kubectl create deployment hello-world-rest-api --image=drmodi/hello-world-rest-api:0.0.1.RELEASE
kubectl expose deployment hello-world-rest-api --type=LoadBalancer --port=8080
```

## Installation Guides

#### Required Tools

- Java 8+
- Eclipse - Recent Version 
- Maven
- Git
- Docker
- Kubernetes
- ELB CLI
- Google Cloud Account

## Kubernetes

Architectures are moving towards Microservices and Cloud. Docker makes it easy to containerize microservices. Kubernetes makes it easy to manage clusters with 1000's of containers running 1000's of microservices. Google Kubernetes Engine (GKE) makes it super easy to create Kubernetes Clusters. 

You will implement Service Discovery, Centralized Configuration, Distributed Tracing and Load Balancing for Spring Boot Microservices deployed in Kubernetes Clusters.

You will learn to use Helm Charts, Istio Service Mesh, Google Stackdriver and Spring Cloud Kubernetes to play with Java Microservices on Kubernetes.

You will be using containerizing (using Docker) and deploying a variety of projects to Kubernetes Clusters. These projects are created with  Spring Boot (REST API Framework), Spring (Dependency Management), Spring Security (Authentication and Authorization - Basic and JWT), BootStrap (Styling Pages), Maven (dependencies management), Eclipse (Java IDE) and Tomcat Embedded Web Server.


### Commands 

```

docker run -p 8080:8080 drmodi/hello-world-rest-api:0.0.1.RELEASE

kubectl create deployment hello-world-rest-api --image=drmodi/hello-world-rest-api:0.0.1.RELEASE
kubectl expose deployment hello-world-rest-api --type=LoadBalancer --port=8080
kubectl scale deployment hello-world-rest-api --replicas=3
kubectl delete pod hello-world-rest-api-58ff5dd898-62l9d
kubectl autoscale deployment hello-world-rest-api --max=10 --cpu-percent=70
kubectl edit deployment hello-world-rest-api #minReadySeconds: 15
kubectl set image deployment hello-world-rest-api hello-world-rest-api=drmodi/hello-world-rest-api:0.0.2.RELEASE

gcloud container clusters get-credentials drmodiutes-cluster --zone us-central1-a --project solid-course-258105
kubectl create deployment hello-world-rest-api --image=drmodi/hello-world-rest-api:0.0.1.RELEASE
kubectl expose deployment hello-world-rest-api --type=LoadBalancer --port=8080
kubectl set image deployment hello-world-rest-api hello-world-rest-api=DUMMY_IMAGE:TEST
kubectl get events --sort-by=.metadata.creationTimestamp
kubectl set image deployment hello-world-rest-api hello-world-rest-api=drmodi/hello-world-rest-api:0.0.2.RELEASE
kubectl get events --sort-by=.metadata.creationTimestamp
kubectl get componentstatuses
kubectl get pods --all-namespaces

kubectl get events
kubectl get pods
kubectl get replicaset
kubectl get deployment
kubectl get service

kubectl get pods -o wide

kubectl explain pods
kubectl get pods -o wide

kubectl describe pod hello-world-rest-api-58ff5dd898-9trh2

kubectl get replicasets
kubectl get replicaset

kubectl scale deployment hello-world-rest-api --replicas=3
kubectl get pods
kubectl get replicaset
kubectl get events
kubectl get events --sort.by=.metadata.creationTimestamp

kubectl get rs
kubectl get rs -o wide
kubectl set image deployment hello-world-rest-api hello-world-rest-api=DUMMY_IMAGE:TEST
kubectl get rs -o wide
kubectl get pods
kubectl describe pod hello-world-rest-api-85995ddd5c-msjsm
kubectl get events --sort-by=.metadata.creationTimestamp

kubectl set image deployment hello-world-rest-api hello-world-rest-api=drmodi/hello-world-rest-api:0.0.2.RELEASE
kubectl get events --sort-by=.metadata.creationTimestamp
kubectl get pods -o wide
kubectl delete pod hello-world-rest-api-67c79fd44f-n6c7l
kubectl get pods -o wide
kubectl delete pod hello-world-rest-api-67c79fd44f-8bhdt

kubectl get componentstatuses
kubectl get pods --all-namespaces

gcloud auth login
kubectl version
gcloud container clusters get-credentials drmodiutes-cluster --zone us-central1-a --project solid-course-258105

kubectl set image deployment hello-world-rest-api hello-world-rest-api=drmodi/hello-world-rest-api:0.0.4-SNAPSHOT

kubectl rollout history deployment hello-world-rest-api
kubectl set image deployment hello-world-rest-api hello-world-rest-api=drmodi/hello-world-rest-api:0.0.4-SNAPSHOT --record

kubectl rollout history deployment hello-world-rest-api
kubectl rollout status deployment hello-world-rest-api
kubectl rollout undo deployment hello-world-rest-api --to-revision=3
kubectl rollout status deployment hello-world-rest-api
kubectl rollout undo deployment hello-world-rest-api --to-revision=3
kubectl rollout status deployment hello-world-rest-api
kubectl rollout history deployment hello-world-rest-api
kubectl get pods
kubectl logs hello-world-rest-api-67c79fd44f-d6q9z
kubectl logs hello-world-rest-api-67c79fd44f-d6q9z -f

kubectl get deployment hello-world-rest-api
kubectl get deployment hello-world-rest-api -o wide
kubectl get deployment hello-world-rest-api -o yaml
kubectl get deployment hello-world-rest-api -o yaml > deployment.yaml
kubectl get service hello-world-rest-api -o yaml
kubectl get service hello-world-rest-api -o yaml > service.yaml

kubectl delete all -l app=hello-world-rest-api
kubectl get all
kubectl apply -f deployment.yaml
kubectl get all

kubectl diff -f deployment.yaml 
kubectl apply -f deployment.yaml 
kubectl delete all -l app=hello-world-rest-api
kubectl get all -o wide

mvn clean install
docker push drmodi/todo-web-application-h2:0.0.1-SNAPSHOT
kubectl delete all -l app=hello-world-rest-api

kubectl get pods
kubectl get pods --all-namespaces
kubectl get pods -l app=todo-web-application-h2
kubectl get pods -l app=todo-web-application-h2 --all-namespaces
kubectl get services --all-namespaces
kubectl get services --all-namespaces --sort-by=.spec.type
kubectl get services --all-namespaces --sort-by=.metadata.name
kubectl cluster-info
kubectl top node
kubectl top pod

kubectl get services
kubectl get svc
kubectl get ev
kubectl get rs

kubectl get ns
kubectl get nodes
kubectl get no
kubectl get po

docker run --detach --env MYSQL_ROOT_PASSWORD=dummypassword --env MYSQL_USER=todos-user --env MYSQL_PASSWORD=dummytodos --env MYSQL_DATABASE=todos --name mysql --publish 3306:3306 mysql:5.7
docker run -p 8080:8080 drmodi/todo-web-application-mysql:0.0.1-SNAPSHOT
docker run -p 8080:8080 --link=mysql --env RDS_HOSTNAME=mysql drmodi/todo-web-application-mysql:0.0.1-SNAPSHOT

docker-compose --version
docker-compose up

brew install kompose
kompose convert

kubectl delete all -l app=todo-web-application-h2

kubectl apply -f mysql-database-data-volume-persistentvolumeclaim.yaml,mysql-deployment.yaml,mysql-service.yaml
kubectl get svc
kubectl apply -f todo-web-application-deployment.yaml,todo-web-application-service.yaml
docker push drmodi/todo-web-application-mysql:0.0.1-SNAPSHOT
kubectl logs todo-web-application-b65cc44d9-7h9pr -f

kubectl apply -f mysql-service.yaml
kubectl get pv
kubectl get pvc
kubectl describe pod/mysql-5ccbbbdcd8-5zjqg 

kubectl create configmap todo-web-application-config --from-literal=RDS_DB_NAME=todos
kubectl get configmap todo-web-application-config
kubectl describe configmap/todo-web-application-config

kubectl edit configmap/todo-web-application-config
kubectl scale deployment todo-web-application --replicas=0
kubectl scale deployment todo-web-application --replicas=1

kubectl edit configmap/todo-web-application-config
kubectl apply -f todo-web-application-deployment.yaml 
kubectl edit configmap todo-web-application-config
kubectl scale deployment todo-web-application --replicas=0
kubectl scale deployment todo-web-application --replicas=1

kubectl create secret generic todo-web-application-secrets --from-literal=RDS_PASSWORD=dummytodos
kubectl get secret/todo-web-application-secrets
kubectl describe secret/todo-web-application-secrets
kubectl apply -f todo-web-application-deployment.yaml 

kubectl delete -f mysql-database-data-volume-persistentvolumeclaim.yaml,mysql-deployment.yaml,mysql-service.yaml,todo-web-application-deployment.yaml,todo-web-application-service.yaml

apiVersion: v1
data:
  RDS_DB_NAME: todos
  RDS_HOSTNAME: mysql
  RDS_PORT: "3306"
  RDS_USERNAME: todos-user
kind: ConfigMap
metadata:
  name: todo-web-application-config
  namespace: default

cd /drmodiutes/git/kubernetes-crash-course/04-currency-exchange-microservice-basic 
mvn clean install
docker push drmodi/currency-exchange:0.0.1-RELEASE
kubectl apply -f deployment.yaml
curl 34.67.103.178:8000/currency-exchange/from/USD/to/INR

kubectl create configmap currency-conversion --from-literal=YOUR_PROPERTY=value --from-literal=YOUR_PROPERTY_2=value2

kubectl autoscale deployment currency-exchange --min=1 --max=3 --cpu-percent=10 
kubectl get events
kubectl get hpa
kubectl get hpa -o yaml
kubectl get hpa -o yaml > 01-hpa.yaml
kubectl get hpa currency-exchange -o yaml > 01-hpa.yaml

kubectl set image deployment hello-world-rest-api --image=drmodi/hello-world-rest-api:0.0.4-SNAPSHOT
kubectl apply -f ingress.yaml
kubectl get ingress
kubectl describe gateway-ingress
kubectl describe gateway gateway-ingress
kubectl describe ingress gateway-ingress
kubectl apply -f rbac.yml
 
docker push drmodi/currency-conversion:0.0.5-RELEASE

kubectl create configmap currency-conversion --from-literal=YOUR_PROPERTY=value --from-literal=YOUR_PROPERTY_2=value2

kubectl describe configmap/currency-conversion


kubectl label namespace default istio-injection=enabled

kubectl get svc --namespace istio-system
kubectl apply -f 01-helloworld-deployment.yaml 
kubectl apply -f 02-creating-http-gateway.yaml 
kubectl apply -f 03-creating-virtualservice-external.yaml 
kubectl get svc --namespace istio-system
kubectl get svc istio-ingressgateway --namespace istio-system
kubectl scale deployment hello-world-rest-api --replicas=4
kubectl delete all -l app=hello-world-rest-api
kubectl apply -f 04-helloworld-multiple-deployments.yaml 
kubectl apply -f 05-helloworld-mirroring.yaml 
kubectl apply -f 06-helloworld-canary.yaml 
watch -n 0.1 curl 35.223.25.220/hello-world

gcloud container clusters get-credentials drmodiutes-cluster-istio --zone us-central1-a --project solid-course-258105
kubectl create namespace istio-system
curl -L https://git.io/getLatestIstio | ISTIO_VERSION=1.2.2 sh -
ls istio-1.2.2
ls istio-1.2.2/install/kubernetes/helm/istio-init/files/crd*yaml
cd istio-1.2.2
for i in install/kubernetes/helm/istio-init/files/crd*yaml; do kubectl apply -f $i; done
helm template install/kubernetes/helm/istio --name istio --set global.mtls.enabled=false --set tracing.enabled=true --set kiali.enabled=true --set grafana.enabled=true --namespace istio-system > istio.yaml
kubectl apply -f istio.yaml
kubectl get pods --namespace istio-system
kubectl get services --namespace istio-system


docker push drmodi/currency-exchange:3.0.0-RELEASE
kubectl apply -f deployment.yaml 
kubectl apply -f 11-istio-scripts-and-configuration/07-hw-virtualservice-all-services.yaml 
kubectl get secret -n istio-system kiali
kubectl create secret generic kiali -n istio-system --from-literal=username=admin --from-literal=passphrase=admin
kubectl get svc --namespace istio-system


gcloud container clusters get-credentials helm-cluster --zone us-central1-a --project solid-course-258105
helm init
kubectl get deploy,svc tiller-deploy -n kube-system
clear
unzip 12-helm.zip
ls helm-tiller.sh
chmod +x helm-tiller.sh

gcloud container clusters get-credentials helm-cluster --zone us-central1-a --project solid-course-258105
./helm-tiller.sh
cat helm-tiller.sh 
kubectl get deploy,svc tiller-deploy -n kube-system
helm install ./currency-exchange/ --name=currency-services
helm install ./currency-conversion/ --name=currency-services-1
helm install ./currency-conversion/ --name=currency-services-3 --debug --dry-run
helm history currency-services-1
helm upgrade currency-services-1 ./currency-conversion/
helm rollback currency-services-1 1
helm upgrade currency-services-1 ./currency-conversion/ --debug --dry-run
helm upgrade currency-services-1 ./currency-conversion/
helm history currency-services-1

```
## Notes

								Kubernates for Java Developers on Google Cloud
								~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
								 
> Kubernetes: It is resource manager, managing resources like server, cluster, etc..
	- Servers are in the cloud meaning they are virtul servers, different cloud provider called them different
		Such as AWS - Called Elastic Compute Cloud (EC2)
				Azure - Virtual Machine
				GCP - Compute Engine
					Kubernetes - Nodes (uses generic terminology)
					
> GKE: Google Kubernetes Engine:

> Cluster: Combination of Nodes (worker nodes) + Master Nodes (Management Work)
	- Kubernetes runs thousand of the Nodes (servers)
	- To manage thousands of nodes, require Manager/Master Node(s). Typically one master node, but to achieve high
	  availability we need master nodes
	- Worker Node(s): Run your applications
	- At high level: contains nodes which manage by Manager node.

> Login to GCP -> Using jmcs account -> Create DRM-GKE-CRASH-COURSE project -> Create Kubernetes Engine -> Created standard cluster called drmodi-std-cluster with default 3 nodes and default configuration such as region, kubernetes latest default version, defult CPU, Memory and Storage config.

> Kubernetes Fun Facts:
	- K8S: abbriviated form
	- Koo-Ber-Net-Eez
	- Logo - Helmsman of ship - somebody providing direction to ship (greek means)
	- Kubernets on cloud:
		- Azure: AKS : Azure Kubernetes Service
		- AWS: EKS : Elastic Kubernetes Service
		- GCP: GKE: Google Kubernetes Engine

> Activate Cloud Shell: Deploying Application to kubernetes cluster: Using command line. GCP provides the command line, no downloads. On right side top.


> Cluster Connection and Command: 
	- Copy the command from connect
	- Paste that in active shell and use kube controller: Main command to intrect with cluster
		
	Below connect to cluster command is for the reference: always use from the ui.
	-------------
	gcloud container clusters get-credentials drmodi-std-cluster --zone us-central1-a --project drm-gke-crash-course
	
	
	kubectl
	--------
	- It will work with any kubernetes cluster - whether cluster is in local machine, or on datacenter, or on cloud
	- It will be used to deploy application, increase instances of application, deploy new version of the application..etc
	
	(1) Checking version:
			kubectl version
	
	(2) Deploying application from the docker hub:
			kubectl create deployment hello-world-rest-api --image=drmodi/hello-world-rest-api:manual_02
			
			sudo code: kubectl create deployment <<name of the deployment>> --image=<<docker image name>>
		
	(3) Expose Application to outside world
			kubectl expose deployment hello-world-rest-api --type=LoadBalancer --port=8080
		
		Check the status by going to the services & ingress section, will find the exposed url as well.
	
		
	(4) Events - Which are performed during creation of clusters, pod, replica sets, etc..
			kubectl get events
		
	(5) Command for getting pods (both plural or singular can be used in command)
			kubectl get pods
			kubectl get pod
		
	(6) Command for getting replica sets (both plural or singular can be used in command)
			kubectl get replicaset
			kubectl get rs
	
	(7) Command for getting deployments and Services (both plural or singular can be used in command)
			kubectl get deployment
			kubectl get Service
			
	(8) Find the eventes performed:
			kubectl get events --sort-by=.metadata.creationTimestamp
			

> Kubernetes:
	- It is uses single responsibility principle, one concept one responsibility
	- Pod, ReplicaSet, Deployments, Service, all will play important role
	- Like Kubectl create deployment command ==> deployment, replicaset and pod
	- Same way kubectl expose deployment ==> service
	- These all in combinantion they provide Kubernetes to perform following:
		- Manage workload
		- Provide external access to workload
		- Enable scalling
		- Enable zero downtime deployments


> Pods: 
	- Most important and smallest deployable unit in Kubernetes (containers are smallest we think but pod in kubernetes)
	- Containers can't be created witout pods, actually they live in a pod
	- Pod contains mulitple containers, all present containers in pod share the resources, within the same pod
	  container talks to each other using localhost.
	- Kubernetes single node/host can contain mulitple pods and each of these pods contain multiple containers.
	- These pods can be from different application or from the same application.
	  
	
	(1) Pod info:
			kubectl get pods -o wide
		Provide details with Name, readiness, IP address, Age, Status, Node, etc.. explain readiness 1/1 meaning number
		of container are present in that specific pod and how many of them are ready.
		
	(2) Explain what is Pod:
			kubectl explain pods
		
		Pod is a collection of containers that can run on a single node/host. This resource is created by clients and
		scheduled onto hosts.
		
	(3) Get the more depth information/describe pod:
			kubectl describe pod <<pod name>>
		To find the pod name
			kubectl get pods
		
		Details contain:
		---------------
		  - Node name of specific pod
		  - Namespace: default being used, but can be used for isolation
		  		- Its provide the isolation from part of the cluster from the other part of the cluster
				- Meaning DEV and QA both environment running on same cluster, so to seperate the resources/servers
				  for Dev and QA can be done through namespace. 
				  
		  - Labels: app=<<app name as label>>
		  	 	- Pod, replicaset, deployment, service, these all are linked using selectors and Labels
				- So it is important
				
		  - Annotation: metainformation for pods, like release id, build id, author name.
		  - Status: running
		  
		  
		Note: Provides a way to put containers together, give them an ip address, also provide categorization them
		      using labels.
			  
	(4) Delete pod
			kubectl delete pods <<pod name>>
			
		To get the pod name: kubectl get pods -o wide
			  
			  
> ReplicaSets:
	- Replicasets ensure specified number of pods are running all the time (called desired in replicaset info)
	
	(1) Get replicaset info:
			kubectl get replicaset
		
		Note: desired should be 1.
			
	(2) How to scale pods for specific app:
			kubectl scale deployment hello-world-rest-api --replicas=3
			
	(3) Now check the replica set info and desired will be 3 due to step 2.
	
	(4) Explain what is Replica set:
			kubectl explain replicaset
			
			
			
> Deployments: 
	- Important to update the release of the applications, without downtime.

	- Replicaset details
		 kubectl get rs -o wide
	
	 Images: name of the docker image
	 Contianers: name of the deployment
	 Desired: no of the pods needs to maintain by the rs
	 selector: app name, app=<<app name label name>>,selector
	 
	 - Updating new image or version of the application
		
		kubectl set image deployment hello-world-rest-api hello-world-rest-api=hello-world-rest-api:0.0.1-SNAPSHOT	
		
		Sudo:		
		kubectl set image deployment <<name of the deployment>> <<container name>>=<<new version of image name>>
		
		To get all above information:
			kubectl get deployments (to get deployment name)
			kubectl describe pods <<pod name>> (to get pod name: kubectl get pods, then get container name and image name from
			 describe command.)
			 
	- Always run
		cubectl get events --sort-by=.metadata.creationTimestamp
	 
	 - Behind the scene it is using default strategy rolling update policy: meaning if 5 instances of v1 are running then it
	   will update to v2 one pod at a time, so once launch the pod with v2 and when it is up and running will reduce the v1 pods.
	   
	   
> Services:
	- If replica set is set to have 3 pods all the time, and if pod being deleted new pod will be created. But that pod will
	 not have the same ip address. However that doesnt have any impact on consumer side and they still getting response from
	 the same endpoints.
	 
	- Service was created as part of the expose deployment, where type was defined as LoadBalancer
	
	(1) Get info:
			kubectl get services
			
	- To see GKE created load balancer, search in GCP console about load balancer and all needed information will appears.
	
	
	

Master Node and WorkerNode/Node.
---------------------------------
	- To get all node componentstatuses health check:
		kubectl get componentstatuses
	
	
	
	
	
> Deployments: Yaml
---------------------------

- To see the history of the deployment
	kubectl rollout history deployment <<deployment name>>
	
	in order to see the change-cause, --record should be provided during new version deployment as described below

- To check the latest deployment status
	kubectl rollout status deployment <<deployment name>>
	
- To revert the deployment
	kubectl rollout undo deployment <<deployment name>> --to-revision=<<revision number>>
	
	to get revision number run the history command and retrive the previously deployed version, revision numebr.
	
- To see all the details about deployments in yaml file.

	kubectl get deployments <<deployment name>> -o yaml
	kubectl get deployments <<deployment name>> -o wide (for brief summary)
	
	download to local machine for view instead of looking at terminal:
		sudo:kubectl get deployment <<deployment-name>> -o yaml > deployment.yaml
		
		kubectl get deployment hello-world-api -o yaml > deployment.yaml
		
- Same way to see all about exposed deployment, or services:
	kubectl get service hello-world-rest-api -o yaml > services.yaml
	

Note: Also we can update yaml file and apply back to GKE.

- To apply changed yaml file:
	kubectl apply -f deployment.yaml
	
		
	
	
	
Application Logs:
----------------

	- Application logs:
			kubectl logs <<pods name>>  (to get pods name kubectl get pods)
	
	- to follow the logs
			kubectl logs <<pods name>> -f
			
	
	
	
	
Gcloud Active Shell in browser:
-------------------------------
	(1) Watch command, needs to be install in local but already available in gcloud active shell
			sudo:
			watch curl <<application url>> (from services&ingress)
			
			watch curl http://34.67.90.204:8080/hello-world
			
			to send request every 100 ms: (1/10 second)


	
	

Reviewing all the details on KubeCtl
-------------------------------------
	(1) Reviewing all Pods, Services, Replicasets, deployments on GKE
		
		kubectl get all
		
	(2) Removing all with the lable
		sudo
		kubectl delete all -l app=<<label name>>
		
		kubectl delete all -l app=hello-world-rest-api
		
		Note:
		- will delets pods->services->deployment->replicasets
		- After removing all make sure running get all only GKE cluster should be running.
		
		
		
*******************************
*  Understanding Yaml
* ******************************	

Deployment:
----------
- To find the difference between previously deployed yaml file vs existing yaml
	kubectl diff -f deployment.yml
	
- imagePullPolicy: Always | IfNotPresent: based on policy image will be downloaded

- minReadySeconds: values in seconds, it will wait 45 seconds for new pods before routing the requests, so it will helpful to minimize the downtime

- redinessProbe:
	> before routing traffic make sure pod is ready to receive traffic

- livenessProbe:
	> It will help to health check, when multiple instances are running.
	

- resources: to manage the minimum and maximum of resources can be allocated


Service & Ingress:
---------------
- Type: 
	> LoadBalancer - used for the service to balance the load accross the pods
	> ClientIP - Available to the cluster only and mainly used internal resources such as DB, fileSystem storage..etc
	> NodePort: 

	
	
	
	
*************************
More Commands:

(1) Get all the pods from all the namespace
		kubectl get pods --all-namespaces
		
(2) Filter the pods based on label
		kubectl get pods -l app=todo-web-application-h2
		kubectl get pods -l app=todo-web-application-h2 --all-namespaces
		
(3) Get all the services froma all the namespaces
		kubectl get services --all-namespaces

(4) Sort services by types
		kubectl get services --all-namespaces --sort-by=.spec.type (spec defined in yaml file, type like loadbalancer)
		
		note: similarly search can be done based on any of the yaml file data.

(5) Get GKE cluster info
		kubectl cluster-info
		
		get more info - it will dump lot of information
			kubectl cluster-info dump
			
(6) Get top Node/Compute engine, pods - based on utilizations.
		kubectl top node
		kubectl top pod
		
(7) Shortcuts
	kubectl get svc (services)
	kubectl get rs (replicaset)
	kubectl get ns (namespaces)
	kubectl get no (for nodes)
	kubectl get po (for pods)
	

	
	
	
**************************************************************
*  Converting docker-compose file to Kubernetes Kompose
**************************************************************

> url for tool: kompose.io/installation

> run brew install compose

> After installation done, cd to the directory where docker-compose.yaml exist and run below command

	kompose convert
	
	
	
*********************************************************
	Google Cloud Storage
*********************************************************

- AWS: EBS Elastic Block Storage
- GCEPD: Google Compute Engine Persistent disk

Using PersistentVolumeClaim yaml - Linked the volume	
	
(1) Command to see Persitent Volume
		kubectl get pv
	
(2) Command to see persitent volume claim
		kubectl get pvc
	
- PV: persitent volume, is how we map external storage to GCP cluster. Meaning Kubernetes clusters access to disk. 
	  PV shared accross the same cluster.
- PVC: persitent volume claim, is how Pod can ask for the persistent volume. 
		Deployments, pods access through the PVC.
		
		
- Access the database: Changing type from LoadBalancer to ClusterIP
--------------------------------------------------------------------
	Using LoadBalancer as type in configuration of mysql db service.yaml, will allow anybody to talk to the database.
	
	Since db is our internal application, so it would be good to make it to "clusterip", so only the application 
	which are in Kubernetes cluster would be able to talk to it.
	
	in order to do that, existing service need to be removed:
		- kubectl delete services mysql
	
	Make chages to yaml file and update sevice type to ClusterIP and run Apply again
		- kubectl apply -f mysql-service.yaml
	
	
*********************************************************
			CONFIG-MAPS and SECRETS, 
*********************************************************
Config Map:
-----------
- Centralized configuration provided by kubernetes. Called Config map. So typical configuration are stored in config map and the credentials are stored in secrets.

- It allows us to set all the application configuration at the configmap and in application only the reference is there. 

- Command:
		kubectl create configmap todo-web-application-config --from-literal=RDS_DB_NAME=todos
		
- To see all the details of the config
	kubectl describe configmap/todo-web-application-config (to retrive name of the configmap kubectl get configmap)
		
- To edit the config map:
	kubectl edit configmap/todo-web-application-config (opens in vi editor, i insert, :wq save and exit)
	
- Now how to restart application so it take effect of the updated config. One important thing in Kubernetes it is always declarative and not the imperative style, meaning can not able to specify the command like stop the application, start or restart the application. one of the way is decreasing the replicas and increasing the replicas.
		
	Decrease: kubectl scale deployment todo-web-application --replicas=0
	
- To delete the configmap
	kubectl delete configmap <<name of the secret>>
	

Secrets:
--------
- It is being used to store the credentials, like password. Here it is created generic entry
	kubectl create secret generic todo-web-application-secret --from-literal=RDS_PASSWORD=dummytodos	
	
- To delete the secrets
	kubectl delete secret <<name of the secret>>
	
	
Ingress:
--------
	- Loadbalancer is one of the costly component in cloud, since it has to be up and running all the time.
	- So overcome this problem, ingress is being used, so based on the uri context value it will inturn route traffic to 
	  pods.
	- it is called gateway-ingress
	- See in GCP console: search LoadBalancing => Find gateway-ingress
	- After ingress up, test the service by removing the host and port from the url and provide the ingress-gateway ip
	- Once all looks good then delete the loadbalancer, also update the deployment.xml with type to NodePort from LoadBalancer
	
	
		
	
	
	
	
*********************************************************
				Microservice 
*********************************************************	
	
Challenges:
-----------
	> Bounded context: Identifying the right context for the service, 
		- involve evolutionary steps due to business logic.
		- Find out right boundries for the service.
	
	> Configuration Management:
		 - Many microservices and across many environment,
		 - Managing config for each services, simplifying this.
	
	> Dynamic Scale Up and Scale down:
		- dymically distribute the load to active instances of the services
		
	> LoadBalancing:
		
	> Visibility:
		- want to have great visibility for what happening in behind the scene for the each services
		- centerlized logs, debug, and all services are up and running.
	
	> Pack of Cards:
		- How can we prevent the 1 or few service down, taking entire architecture down
		- building falut tolerance



springcloud with kubernetes:
****************************

		
Spring Cloud Starter Sleuth:
----------------------------
- To allows to trace the request across the microservice


Service Discovery
-------------------------

	 Using Environment Variable:
	 ----------------------------
		- By default when service start in the kubernetes, it will create evironment variables for each service
			like for Service Host:
				<<Take the service name, conver into capital letter>>_SERVICE_HOST
				ex. CURRENCY_EXCHANGE_SERVICE_HOST and value will internal ip assign to instance of this services.
			
			So in application we can assign this variable to replace the host dynamically for proxy services (inside 
			feignClient configuration.)

			- Same way Port are also assigned. <<service_name>>_SERVICE_PORT
		
			Note: this it is not the ideal way to do service discovery, because environment variables are always setup when
			service coming up, in case of the service comeup first which calling other service and is not up, then
			environment variable will not be setup so it will have problem. Ideal ways to use kubernetes service discovery
			or dns.
	
	Kubernetes Service Discovery based on DNS:
	-------------------------------------------
		- By default, kubernetes register all the services as below:
			http://<<Service_Name>>
			ex: http://currency-exchage
	
			- So configure this in client deployment.yaml, so it will recognized it dyanmically.
			- Also can be done through using profiles:
	


Ingress:
--------
	- Loadbalancer is one of the costly component in cloud, since it has to be up and running all the time.
	- So overcome this problem, ingress is being used, so based on the uri context value it will inturn route traffic to 
	  pods.
	- it is called gateway-ingress
	- See in GCP console: search LoadBalancing => Find gateway-ingress
	- After ingress up, test the service by removing the host and port from the url and provide the ingress-gateway ip
	- Once all looks good then delete the loadbalancer, also update the deployment.xml with type to NodePort from LoadBalancer
	
	
	
	
Ribbon Client - Creating client side loadbalancing 
--------------------------------------------------
- In previous step feign client which inturn findout/discover url from the default kubernetes registry from DNS name 
- Also it was defined as environment value under the deployment.yaml
	 env: //CHANGE
	   - name: CURRENCY_EXCHANGE_URI
	     value: http://currency-exchange
	
@FeignClient(name = "currency-exchange", url = "${CURRENCY_EXCHANGE_URI:http://localhost}:8000")//http://currency-exchange

- Using Ribbon now service will discover based on the service/deployment/app name defined for the services while running in kubernetes engine.
	@FeignClient(name = "currency-exchange")//Kubernetes Service Name
	@RibbonClient(name = "currency-exchange")

- Before using with feign, discovery was done through kubernetes and environment setup in deployment.yaml, as soon as the ribbon applied, it started failing with below error. 

Resolution is: created "ClusterRoleBinding" that enable ribbon to be able to talk to the kubernetes discovery api. Using 
			clusterRoleBinding mapping default service account which is already created to cluster role with acccess of view 
			on the API group. 



Error:
*****
Whitelabel Error Page
This application has no explicit mapping for /error, so you are seeing this as a fallback.

Tue Feb 18 23:54:40 GMT 2020
There was an unexpected error (type=Internal Server Error, status=500).
Error creating bean with name 'ribbonLoadBalancingHttpClient' defined in org.springframework.cloud.netflix.ribbon.apache.HttpClientRibbonConfiguration: Unsatisfied dependency expressed through method 'ribbonLoadBalancingHttpClient' parameter 2; nested exception is org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'ribbonLoadBalancer' defined in org.springframework.cloud.netflix.ribbon.RibbonClientConfiguration: Bean instantiation via factory method failed; nested exception is org.springframework.beans.BeanInstantiationException: Failed to instantiate [com.netflix.loadbalancer.ILoadBalancer]: Factory method 'ribbonLoadBalancer' threw exception; nested exception is io.fabric8.kubernetes.client.KubernetesClientException: Failure executing: GET at: https://10.122.0.1/api/v1/namespaces/default/endpoints/currency-exchange. Message: Forbidden!Configured service account doesn't have access. Service account may have been revoked. endpoints "currency-exchange" is forbidden: User "system:serviceaccount:default:default" cannot get resource "endpoints" in API group "" in the namespace "default".
	
	
	
Configmap with Spring Cloud Config:
-----------------------------------
- If we define the configuration in application.property file and we have created the configmap in kuberentes with the same name then it will be picked up automatically during pods/application comesup.
	spring.application.name=currency-conversion
	
	Advantages:
		- the biggest one is that, we not need to maintain the configuration to lookup the configmap in deployment.yaml, and
		 whenever there is any update, we need to do the apply of deployment.yaml.
		- By default application, it will look up if we kept the spring application name and the configmap name same.
		
			just for an example, which we have done, web-project for config map
	
				 - env:
				        - name: RDS_DB_NAME
				#          value: todos
				          valueFrom:
				            configMapKeyRef:
				              key: RDS_DB_NAME
				              name: todo-web-application-config
							  

	




	

******************************************************
*****				Auto Scaling				******
******************************************************

Cluster Auto Scaling
----------------------
- Increasing nodes in cluster. will defined at during cluster creations.

	gcloud container clusters create example-cluster \
			--zone us-central1-a \
			--node-locations us-central1-a,us-central1-b,us-central1-f \
			--num-nodes 2 --enable-autoscaling --min-nodes 1 --max-nodes 4



Vertical Pod Auto Scaling
---------------------------
- Increasing resources in pods, meaning increasing the resources CPU and Memory from available at pods. Meaning increasing the
size of the pod.

Available in GCP version 1.14.7-gke.10 or higher and in 1.15.4-gke.15 or higher

Enable on Cluster:
	gcloud container clusters create [CLUSTER_NAME] --enable-vertical-pod-autoscaling --cluster-version=1.14.7
	gcloud container clusters update [CLUSTER-NAME] --enable-vertical-pod-autoscaling


Configure VPA: 
	apiVersion: autoscaling.k8s.io/v1
	kind: VerticalPodAutoscaler
	metadata:
  	  name: currency-exchange-vpa
	spec:
  	  targetRef:
    	apiVersion: "apps/v1"
    	kind:       Deployment
    	name:       currency-exchange
  	  updatePolicy:
    	updateMode: "Off"


Get Recommendations: 
using update mode off, will generate the recommedation from the kubernetes based on the usage.
	kubectl get vpa currency-exchange-vpa --output yaml



Horizontal Pod Auto Scaling
-------------------------------
- Based on usage increasing number pods. Meaning in Node if allocated resources are not fully utilized and there is still rooms for increasing number of pods. 

kubectl autoscale deployment currency-exchange-service --max=3 --min=1 --cpu-percent=50


	
	
	
******************************************************
*****	Monitoring Using GCP StackDriver		******
******************************************************

Note: It is cloud specific monitoring.

Microservice Continue: With new cluster: StackDriver: Monitoring
------------------------------------------------------------------
- Provides number of options among of those, one important one is looking at the log and trace the request/logs and helps to determine which instance have processed the request, for debugging issues.

- Create new cluster with the opetiong which is defined at the bottom of the page called,
	  Enable Stackdriver Kubernetes Engine Monitoring

- Aftet creating cluster - For given account, enable the stack driver API. Type API and Services in general search bar in GCP.
Click on Enable API, again search and enable follwoing API
	 - Stackdriver API then Enable stackdriver API
	 - stackdriver monitoring API.
	 - Stackdriver logging API
	 - Stackdriver Trace API
	 - Stackdriver Error Reporting API.
	 
	Validate by going to API & Services in search bar..all are listed in the list of apis.
	
- Now run the services and see the trace list by searching StackDriver -> It will further launch the monitoring dashboard.

- Under kubernetes engine ui -> workload -> container logs -> finding the ID something like "5e4dc65727736b8bf94bfdf43e290a3d"
	and remove all the search criteria in top, go for basic search with the ID, will provide all the logs around this id or 
	perticular request which are tied to this id. This is possible because of sping cloud starter sleuth dependency.










******************************************************
*****			Service Mesh - ISTIO			******
******************************************************
* Cloud Neutral:
* 


- Its sidecar pattern
- Multiple containers on pods, will scaled together so very less service are such needs similar scaling. Also resources
  needed by micro service are different than other microservice.
- Each of the micro services which are deployed in each pods, have need of common functionality, such as service discovery,
  logging, distributed tracing, release automation (release strategy). 
- Instead of building all common functionality into the service / container, having separate service mesh container along 
  with all these containers which address the common functionality.
- All request are routed through a specific container and that’s where this service mesh concept comes into the picture and 
  Istio is the most popular service mesh implementation.Specific container called SideCar
  
Steps Perform: Install istio on cluster
-----------------------------------------
(1) Connect to cluster and istall istio:
	### Connect to kubernetes cluster: on google cloud
	gcloud container clusters get-credentials drm-cluster-istio --zone us-central1-a --project drm-gke-crash-course

	### Create namespace for istio
	kubectl create namespace istio-system

	#### Download istio and apply
	curl -L https://git.io/getLatestIstio | ISTIO_VERSION=1.2.2 sh -
	cd istio-1.2.2 
	for i in install/kubernetes/helm/istio-init/files/crd*yaml; do kubectl apply -f $i; done

(2) Install Istio with components for graphana, prometheus, tracing(jaeger), kiali as subcharts using Helm Charts.

	### Install pre-created templates - helm, Create yml file for istio

helm template install/kubernetes/helm/istio --name istio --set global.mtls.enabled=false --set tracing.enabled=true --set kiali.enabled=true --set grafana.enabled=true --namespace istio-system > istio.yaml

	### Apply created yaml file, istio.yaml has 18,000 lines of configuration.
	kubectl apply -f istio.yaml
	
(3) Verify the installation of istio
	
	to see all the pods which are running under this namespace:
		kubectl get pods --namespace istio-system
		
	to see all the service
		kubectl get services --namespace istion-system


Steps to enable Adding istio side cars in each pods
---------------------------------------------------
(4) Injecting istio side car - in default name space:

	kubectl label namespace default istio-injection=enabled
	

Note:: now if you run below command to see all, notice 2 container running in that pod.
		kubectl get all -o wide 
to see the logs: previously only using the pod name now, pod name -> container name, since side car is running after step 4
		kubectl logs <<pod name>> <<container name>> -f
		
(5) Create istio gateway and virtual services

	list all services which are running for istio
		kubectl get services --namespace istio-system
		
	Note: in list noticed the istio selector with ingressgateway as loadbalancer, now create http-gateway on top of and will redirect all the port80 http traffice to all host which are come under this gateway.
	
	run command to apply gateway yaml file:
		kubectl apply -f 02-creating-http-gateway.yaml
		
	run command to apply virtual service yaml file: which is similar to ingress, where configure the routes.
		kubectl apply -f 03-creating-virtualservice-external.yaml
	
	Now, finds the external ip of the istio-ingressgateway and fire the request.
		
 ******************************************************************************											
 *																			*  
 *												(1) K8S service A			*
 *	istio-gateway --> istio virtual service --> 							*
 *						(configure routes)		(2) K8S service B 			*
 * 																			*
 * 																			*
 ********************************************************************************	
	
Deployment Strategies
----------------------
	
	
	
	Default Release Strategies:
	------------------------------
	- Recreate: will terminate existing pods and launch same number of pods with new version of the service
	- Rolling update:
		- with max surge: 25% - meaning allow total instance like 8 to grow till 10 pods, during new version deployment
		- with max unavailable - 25% - meaning allow total instance like 8 to shrink till 6 pods, during new version deployment
		
	
	
	
	Alternate Deployment Strategies: Blue Green using mirroring concept. - 100 response to user from one version only
	-------------------------------------------------------------------------------------------------------------
	- Mirroring: it allows both verison of the deployment or services are up and running, so complete testing can be perform on
	the new version before taking previous version completely out and making new version live. 
		- Draw back is not possible where db transaction are involved.
		- It can be done, by updating the istio virtual service rule and creating istio desintion rule for mapping different 
		  services.
		
																								(1) K8S service A V1
			istio-gateway --> 		istio virtual service		-->  Istio Destination Rule -->
								(configure routes to services			(ma to different 		(2) K8S service A V2	
								configure weights for subsets)			  services versions)
	

		- So this allow us to send all 100% traffice to version 1 but also it will mirror all the request to v2 as well.
		
		    http:
		      - match:
		          - uri:
		              exact: /hello-world
		        route:
		          - destination:
		              host: hello-world-rest-api
		              subset: v1
		            weight: 100
		        mirror:
		          host: hello-world-rest-api
		          subset: v2
		 
		 - Once followed logs and all looks good on version 2, and to make switch and lets make version V2 live, in order to 
		 do that now remove the mirroring from .yaml file and change destination to V2 in yaml and apply yaml to take effect.

	 	
		
		
		Alternate Deployment Strategies: Canary No mirroring concept. - both versions are live in production
	 	-------------------------------------------------------------------------------------------------------------
		- the only difference in both version
		
		    http:
		      - match:
		          - uri:
		              exact: /hello-world
		        route:
		          - destination:
		              host: hello-world-rest-api
		              subset: v1
		            weight: 90
		          - destination:
		              host: hello-world-rest-api
		              subset: v2
		            weight: 10

			- Slowly slowly increase the percentage of the version and progress as needed.



Spring boot integration with Istio - tracing:
############################################

(1) Add dependencies, opentracing and jaeger
		
		<dependency> <!--CHANGE-->
			<groupId>io.opentracing.contrib</groupId>
			<artifactId>opentracing-spring-cloud-starter</artifactId>
			<version>0.1.7</version>
		</dependency>

		<dependency> <!--CHANGE-->
			<groupId>io.jaegertracing</groupId>
			<artifactId>jaeger-tracerresolver</artifactId>
			<version>0.29.0</version>
		</dependency>



Kiali:
#####
	- It will provide the information of what are the microservices are part of the istio service mesh?
	- How are they connected?
	- How are they perfoming?
	
	- Forward port to see kiali console in local: http://localhost:20001, copy command from github, project 11 readme
		kubectl port-forward \
		    $(kubectl get pod -n istio-system -l app=kiali \
		    -o jsonpath='{.items[0].metadata.name}') \
		    -n istio-system 20001
		
	- Create secret to enable access to kiali console:
		
		kubectl get secret -n istio-system kiali 
		kubectl create secret generic kiali -n istio-system --from-literal=username=kialiAdmin --from-literal=passphrase=kialiAdmin
		
		
		
		
Using Graphana to see prometheus metrics
#########################################

- Prometheus: is storing time series data in database, each moment time with difference timespan, like weather, stock price, etc..

- Graphana is allow to see the stored prometheus data.

Forward port to see kiali console in local: http://localhost:3000, copy command from github, project 11 readme
kubectl -n istio-system port-forward \
    $(kubectl -n istio-system get pod -l app=grafana \
    -o jsonpath='{.items[0].metadata.name}') 3000
		


Jaeger:
###########
 - Distribution of tracing 
 - Implementation of open tracing api.
 Forward port to see kiali console in local: http://localhost:16686, copy command from github, project 11 readme

kubectl port-forward -n istio-system \
    $(kubectl get pod -n istio-system -l app=jaeger \
    -o jsonpath='{.items[0].metadata.name}') 16686












**************************************************************
*  Install Kubernetes Helm	
**************************************************************

- The package manager for kubernetes (called Helm Chart)
	- Help to manage kubernetes application
	- Help to define, install and upgrade even the most complex kubernetes application.
	- Charts are easy to create, version, share and publish, so start using helm and stop copy 
		and paste the many yaml files as we did in last istio project.
		
- Main terminologies:
		- Helm Chart, Repository and Release
- Helm Client <====> Helm Tiller (Server Side)

- Helm client: Install helm in local for client 
- Helm Server: run shell script on helm-tiller.sh for server from the package.
	- First connect to the cluster
	- then run helm-tiller.sh script

	
	 



 
	
	
	
	
	
	
	
*******************************
*  TO SAVE CREDITS ON GCP
* ******************************

	Save Your Free Credits In the cloud, it is best practice to delete the resources when you are not using them.
	If you do not want to delete and create a new cluster every time, you can reduce the cluster size to zero.
	You can reduce cluster node size to zero.

		gcloud container clusters resize --zone us-central1-a drmodi-std-cluster --num-nodes=0

	When you are ready to start again, increase the number of nodes:

		gcloud container clusters resize --zone us-central1-a drmodi-std-cluster --num-nodes=3
		
		
		
Delete Resources using yaml file: 
---------------------------------------
	kubectl delete -f <<list all the yaml files>>
	
	
	
******************************
******************************
	
	
	
	
More Research:
----------------

Type: ClusterIP vs NodePort 
---------------------------


More on Services and Routes:
-----------------------------




Spring Cloud And Kubernetes
----------------------------------
1. course/microservices-with-spring-boot-and-spring-cloud/

2. course/kubernetes-crash-course-for-java-developers/

you have uploaded several videos on spring cloud and Kubernetes. Spring Cloud has code level and Kubernetes has platform level to scale up/down. Both are good in various parameters like distributed tracing, service discovery etc., But Java developers have to do extra effort for all these configurations other than business logic. But I have gone through some sites like we can use both Spring Cloud and Kubernetes. Can you make a video on these differences and a project on both integrations of these for our audience?

Here are the links which I have referred.

1. baeldung.com/spring-cloud-kubernetes

2. cloud.spring.io/spring-cloud-kubernetes/reference/html/

3. salaboy.com/2018/05/24/spring-cloud-kubernetes-example/

4.  stackoverflow.com/questions/40567429/eureka-and-kubernetes

5. dzone.com/articles/microservice-architecture-with-spring-cloud-and-do
	
				
				
	

	
		
	
			
			
	

	
	
		

