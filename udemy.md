# Udemy Mock CKA

Q1.
---
Upgrade the current version of kubernetes from 1.30.0 to 1.31.0 exactly using the kubeadm utility. Make sure that the upgrade is carried out one node at a time starting with the controlplane node. To minimize downtime, the deployment gold-nginx should be rescheduled on an alternate node before upgrading each node.


Upgrade controlplane node first and drain node node01 before upgrading it. Pods for gold-nginx should run on the controlplane node subsequently.

- Cluster Upgraded?
- pods 'gold-nginx' running on controlplane?

Q2.
---
Print the names of all deployments in the admin2406 namespace in the following format:

DEPLOYMENT   CONTAINER_IMAGE   READY_REPLICAS   NAMESPACE

<deployment name>   <container image used>   <ready replica count>   <Namespace>
. The data should be sorted by the increasing order of the deployment name.


Example:

DEPLOYMENT   CONTAINER_IMAGE   READY_REPLICAS   NAMESPACE
deploy0   nginx:alpine   1   admin2406
Write the result to the file /opt/admin2406_data.

Q3.
---
A kubeconfig file called admin.kubeconfig has been created in /root/CKA. There is something wrong with the configuration. Troubleshoot and fix it.


- Fix /root/CKA/admin.kubeconfig

Q4.
---
Create a new deployment called nginx-deploy, with image nginx:1.16 and 1 replica. Next upgrade the deployment to version 1.17 using rolling update.


Image: nginx:1.16

Task: Upgrade the version of the deployment to 1:17

Q5.
---
A new deployment called alpha-mysql has been deployed in the alpha namespace. However, the pods are not running. Troubleshoot and fix the issue. The deployment should make use of the persistent volume alpha-pv to be mounted at /var/lib/mysql and should use the environment variable MYSQL_ALLOW_EMPTY_PASSWORD=1 to make use of an empty root password.


Important: Do not alter the persistent volume.

- Troubleshoot and fix the issues

Q6.
---
Take the backup of ETCD at the location /opt/etcd-backup.db on the controlplane node.

Q7.
---
Create a pod called secret-1401 in the admin1401 namespace using the busybox image. The container within the pod should be called secret-admin and should sleep for 4800 seconds.

The container should mount a read-only secret volume called secret-volume at the path /etc/secret-volume. The secret being mounted has already been created for you and is called dotfile-secret.


Q8.
---
Deploy a pod named nginx-pod using the nginx:alpine image.


Once done, click on the Next Question button in the top right corner of this panel. You may navigate back and forth freely between all questions. Once done with all questions, click on End Exam. Your work will be validated at the end and score shown. Good Luck!

Name: nginx-pod

Image: nginx:alpine

Q9.
---
Deploy a messaging pod using the redis:alpine image with the labels set to tier=msg.


Pod Name: messaging

Image: redis:alpine

Labels: tier=msg

Q10.
---
Create a namespace named apx-x9984574.


Namespace: apx-x9984574

Q11.
---
Get the list of nodes in JSON format and store it in a file at /opt/outputs/nodes-z3444kd9.json.


Task completed



Q12.
---
Create a service messaging-service to expose the messaging application within the cluster on port 6379.


Use imperative commands.

Service: messaging-service

Port: 6379

Type: ClusterIp

Use the right labels

Q13.
---
Create a deployment named hr-web-app using the image kodekloud/webapp-color with 2 replicas.


Name: hr-web-app

Image: kodekloud/webapp-color

Replicas: 2

Q14.
---
Create a static pod named static-busybox on the controlplane node that uses the busybox image and the command sleep 1000.


Name: static-busybox

Image: busybox


Q15.
---
Create a POD in the finance namespace named temp-bus with the image redis:alpine.


Name: temp-bus

Image Name: redis:alpine

Q16.
---
A new application orange is deployed. There is something wrong with it. Identify and fix the issue.


Issue fixed

Q16.
---
Expose the hr-web-app created in the previous task as a service named hr-web-app-service, accessible on port 30082 on the nodes of the cluster.


The web application listens on port 8080.

Name: hr-web-app-service

Type: NodePort

Endpoints: 2

Port: 8080

NodePort: 30082

Q17.
---
Use JSON PATH query to retrieve the osImages of all the nodes and store it in a file /opt/outputs/nodes_os_x43kj56.txt.


The osImage are under the nodeInfo section under status of each node.

Task Completed

Q18.
---
Create a Persistent Volume with the given specification: -

Volume name: pv-analytics

Storage: 100Mi

Access mode: ReadWriteMany

Host path: /pv/data-analytics


Is the volume name set?

Is the storage capacity set?

Is the accessMode set?

Is the hostPath set?

Q19.
---
Take a backup of the etcd cluster and save it to /opt/etcd-backup.db.

Q20.
---
Create a Pod called redis-storage with image: redis:alpine with a Volume of type emptyDir that lasts for the life of the Pod.


Specs on the below.

Pod named 'redis-storage' created

Pod 'redis-storage' uses Volume type of emptyDir

Pod 'redis-storage' uses volumeMount with mountPath = /data/redis

Q.21
---
Create a new pod called super-user-pod with image busybox:1.28. Allow the pod to be able to set system_time.


The container should sleep for 4800 seconds.

Pod: super-user-pod

Container Image: busybox:1.28

Is SYS_TIME capability set for the container?

Q22.
---
A pod definition file is created at /root/CKA/use-pv.yaml. Make use of this manifest file and mount the persistent volume called pv-1. Ensure the pod is running and the PV is bound.


mountPath: /data

persistentVolumeClaim Name: my-pvc

persistentVolume Claim configured correctly

pod using the correct mountPath

pod using the persistent volume claim?

Q23.
---
Create a new deployment called nginx-deploy, with image nginx:1.16 and 1 replica. Next upgrade the deployment to version 1.17 using rolling update.


Deployment : nginx-deploy. Image: nginx:1.16

Image: nginx:1.16

Task: Upgrade the version of the deployment to 1:17

Task: Record the changes for the image upgrade

Q24.
---
Create a new user called john. Grant him access to the cluster. John should have permission to create, list, get, update and delete pods in the development namespace . The private key exists in the location: /root/CKA/john.key and csr at /root/CKA/john.csr.


Important Note: As of kubernetes 1.19, the CertificateSigningRequest object expects a signerName.

Please refer the documentation to see an example. The documentation tab is available at the top right of terminal.

CSR: john-developer Status:Approved

Role Name: developer, namespace: development, Resource: Pods

Access: User 'john' has appropriate permissions

Q25.
---
Create a nginx pod called nginx-resolver using image nginx, expose it internally with a service called nginx-resolver-service. Test that you are able to look up the service and pod names from within the cluster. Use the image: busybox:1.28 for dns lookup. Record results in /root/CKA/nginx.svc and /root/CKA/nginx.pod


Pod: nginx-resolver created

Service DNS Resolution recorded correctly

Pod DNS resolution recorded correctly

Q26.
---
Create a static pod on node01 called nginx-critical with image nginx and make sure that it is recreated/restarted automatically in case of a failure.


Use /etc/kubernetes/manifests as the Static Pod path for example.

static pod configured under /etc/kubernetes/manifests ?

Pod nginx-critical-node01 is up and running

Q27.
---
Create a new service account with the name pvviewer. Grant this Service account access to list all PersistentVolumes in the cluster by creating an appropriate cluster role called pvviewer-role and ClusterRoleBinding called pvviewer-role-binding.
Next, create a pod called pvviewer with the image: redis and serviceAccount: pvviewer in the default namespace.


ServiceAccount: pvviewer

ClusterRole: pvviewer-role

ClusterRoleBinding: pvviewer-role-binding

Pod: pvviewer

Pod configured to use ServiceAccount pvviewer ?

Q28.
---
List the InternalIP of all nodes of the cluster. Save the result to a file /root/CKA/node_ips.


Answer should be in the format: InternalIP of controlplane<space>InternalIP of node01 (in a single line)

Q29.
---
Create a pod called multi-pod with two containers.
Container 1: name: alpha, image: nginx
Container 2: name: beta, image: busybox, command: sleep 4800

Environment Variables:
container 1:
name: alpha

Container 2:
name: beta


Pod Name: multi-pod

Container 1: alpha

Container 2: beta

Container beta commands set correctly?

Container 1 Environment Value Set

Container 2 Environment Value Set

Q30.
---
Create a Pod called non-root-pod , image: redis:alpine

runAsUser: 1000

fsGroup: 2000


Pod non-root-pod fsGroup configured

Pod non-root-pod runAsUser configured

Q31.
---
We have deployed a new pod called np-test-1 and a service called np-test-service. Incoming connections to this service are not working. Troubleshoot and fix it.
Create NetworkPolicy, by the name ingress-to-nptest that allows incoming connections to the service over port 80.


Important: Don't delete any current objects deployed.

Important: Don't Alter Existing Objects!

NetworkPolicy: Applied to All sources (Incoming traffic from all pods)?

NetWorkPolicy: Correct Port?

NetWorkPolicy: Applied to correct Pod?

Q32.
---
Taint the worker node node01 to be Unschedulable. Once done, create a pod called dev-redis, image redis:alpine, to ensure workloads are not scheduled to this worker node. Finally, create a new pod called prod-redis and image: redis:alpine with toleration to be scheduled on node01.


key: env_type, value: production, operator: Equal and effect: NoSchedule

Key = env_type

Value = production

Effect = NoSchedule

pod 'dev-redis' (no tolerations) is not scheduled on node01?

Create a pod 'prod-redis' to run on node01

Q33.
---
Create a pod called hr-pod in hr namespace belonging to the production environment and frontend tier .
image: redis:alpine


Use appropriate labels and create all the required objects if it does not exist in the system already.

hr-pod labeled with environment production?

hr-pod labeled with tier frontend?

Q34.
---
A kubeconfig file called super.kubeconfig has been created under /root/CKA. There is something wrong with the configuration. Troubleshoot and fix it.


Fix /root/CKA/super.kubeconfig

Q35.
---
We have created a new deployment called nginx-deploy. scale the deployment to 3 replicas. Has the replica's increased? Troubleshoot the issue and fix it.


deployment has 3 replicas

