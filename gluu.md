[Gluu and gluu-gateway Installation with couchbase in EKS kubernetes cluster:]{.ul}
===================================================================================

**[EKS Cluster Details:]{.ul}**

Nodes : 2

CPU : 16 (total)

RAM : 64GB (total)

Disk Space : 80GB

Kubernetes Version: v1.18.6

**Gluu Installation steps:**

**mkdir gluu && cd gluu**

**For FQDN-Domain add .crt and .key file in gluu directory as gluu.crt &
gluu.key.**

**wget
<https://github.com/GluuFederation/cloud-native-edition/releases/download/v1.2.20/pygluu-kubernetes-linux.pyz>**

**mv pygluu-kubernetes-linux.pyz pygluu-kubernetes.pyz**

**chmod a+x pygluu-kubernetes.pyz**

**wget
<https://packages.couchbase.com/kubernetes/2.0.1/couchbase-autonomous-operator-kubernetes_2.0.1-linux-x86_64.tar.gz>**

**./pygluu-kubernetes.pyz install**

**Do you accept the Gluu license stated above \[N\] \[y/N\]: y**

**2020-11-07 14:56:35,663 - gluu-common - INFO - Currently supported
versions are :**

**2020-11-07 14:56:35,664 - gluu-common - INFO - Stable version : 4.2**

**2020-11-07 14:56:35,664 - gluu-common - INFO - Development version :
4.2.2_dev**

**Please enter the current version of Gluu or the version to be
installed \[4.2\]:**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| Test Environment Deployments \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| \[1\] Microk8s \[default\] \|**

**\| \[2\] Minikube \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| Cloud Deployments \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| \[3\] Amazon Web Services - Elastic Kubernetes Service (Amazon
EKS)\|**

**\| \[4\] Google Cloud Engine - Google Kubernetes Engine (GKE) \|**

**\| \[5\] Microsoft Azure (AKS) \|**

**\| \[6\] Digital Ocean \[Beta\] \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| Local Deployments \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| \[7\] Manually provisioned Kubernetes cluster \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**Deploy on \[1\]: 3**

**Namespace to deploy Gluu in \[gluu\]:**

**Deploy Cr-Rotate \[N\] \[y/N\]:**

**Deploy Key-Rotation \[N\] \[y/N\]:**

**Deploy Radius \[N\] \[y/N\]:**

**Deploy Passport \[N\] \[y/N\]:**

**Deploy Shibboleth SAML IDP \[N\] \[y/N\]:**

**Deploy Casa \[N\] \[y/N\]: y**

**Deploy fido2 \[N\] \[y/N\]:**

**Deploy scim \[N\] \[y/N\]:**

**oxd server application keystore name \[oxd-server\]:**

**oxd server admin keystore name \[oxd-server\]:**

**Enable oxTrust API \[N\] \[y/N\]:**

**Enable oxTrust Test Mode \[N\] \[y/N\]:**

**Install Gluu Gateway Database mode \[N\] \[y/N\]: y**

**Please enter a namespace for postgres \[postgres\]:**

**Please enter number of replicas for postgres \[3\]:**

**Please enter postgres (remote or local) URL base name. If postgres is
to be installed \[postgres.postgres.svc.cluster.local\]:**

**Please enter a namespace for Gluu Gateway \[gluu-gateway\]:**

**Please enter a namespace for gluu gateway ui \[gg-ui\]:**

**Please enter a user for gluu-gateway postgres database \[kong\]:**

**gluu-gateway-postgres password \[N\*\*\*\#h\]:**

**Confirm password:**

**2020-11-07 14:58:19,926 - gluu-common - INFO - Success!
gluu-gateway-postgres password was set.**

**Please enter a user for gluu-gateway-ui postgres database \[konga\]:**

**gluu-gateway-ui-postgres password \[R\*\*\*\#0\]:**

**Confirm password:**

**2020-11-07 14:58:39,427 - gluu-common - INFO - Success!
gluu-gateway-ui-postgres password was set.**

**Please enter gluu-gateway postgres database name \[kong\]:**

**Please enter gluu-gateway-ui postgres database name \[konga\]:**

**2020-11-07 14:58:45,266 - gluu-prompt-jackrabbit - INFO - Jackrabbit
must be installed. If the following prompt is answered with N it is
assumed the jackrabbit content repository is either installed locally or
remotely**

**Install Jackrabbit content repository \[Y\] \[Y/n\]:**

**Size of Jackrabbit content repository volume storage \[4Gi\]:**

**Please enter Jackrabit admin user \[admin\]:**

**jackrabbit-admin password \[)\*\*\*\*.ivy\--7tahF?8zoJwI\|\]:**

**Confirm password:**

**2020-11-07 14:59:17,308 - gluu-common - INFO - Success!
jackrabbit-admin password was set.**

**Enable Jackrabbit in cluster mode\[beta\] Recommended in production
\[Y\] \[Y/n\]:**

**Please enter a user for jackrabbit postgres database \[jackrabbit\]:**

**jackrabbit-postgres password \[=\*\*\*J@\]:**

**Confirm password:**

**2020-11-07 14:59:31,518 - gluu-common - INFO - Success!
jackrabbit-postgres password was set.**

**Please enter jackrabbit postgres database name \[jackrabbit\]:**

**\[Alpha\] Would you like to use Istio Ingress with Gluu ? \[N\]
\[y/N\]:**

**2020-11-07 14:59:46,527 - gluu-prompt-istio - INFO - Please follow
https://istio.io/latest/docs/ to learn more.**

**2020-11-07 14:59:46,528 - gluu-prompt-istio - INFO - Istio will auto
inject side cars into all pods in Gluus namespace chosen. The label
istio-injection=enabled will be added to the namespace Gluu will be
installed in if the namespace does not exist. If it does please run
kubectl label namespace \<namespace\> istio-injection=enabled**

**\[Alpha\] Would you like to use Istio with Gluu ? \[N\] \[y/N\]:**

**2020-11-07 14:59:48,144 - gluu-prompt-test-env - INFO - A test
environment means that the installer will strip all resource
requirements, and hence will use as much as needed only. The pods are
subject to eviction. Please use at least 8GB Ram , 4 CPU, and 50 GB
disk.**

**Is this a test environment. \[N\] \[y/N\]:**

**Please enter the ssh key path if exists to login into the nodes
created. This ssh key will only be used to delete folders created on the
nodes by the setup if the user uses local volumes \[\~/.ssh/id_rsa\]:**

**2020-11-07 14:59:53,716 - gluu-prompt-common - INFO - Determining OS
type and attempting to gather external IP address**

**2020-11-07 14:59:53,921 - gluu-kubernetes-api - INFO - Getting list of
nodes**

**2020-11-07 14:59:53,936 - gluu-kubernetes-api - INFO - Getting node
tapas-k8s data**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| AWS Loadbalancer type \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| \[1\] Classic Load Balancer (CLB) \[default\] \|**

**\| \[2\] Network Load Balancer (NLB - Alpha) \-- Static IP \|**

**\| \[3\] Application Load Balancer (ALB - Alpha) DEV_ONLY \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**Loadbalancer type \[1\]:**

**Are you terminating SSL traffic at LB and using certificate from AWS
\[N\] \[y/N\]:**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| Persistence layer \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| \[1\] OpenDJ \[default\] \|**

**\| \[2\] Couchbase \|**

**\| \[3\] Hybrid(OpenDJ + Couchbase) \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**Persistence layer \[1\]: 2**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\|Amazon Web Services - Elastic Kubernetes Service (Amazon EKS) \|**

**\| MultiAZ - Supported \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| \[6\] volumes on host \|**

**\| \[7\] EBS volumes dynamically provisioned \[default\] \|**

**\| \[8\] EBS volumes statically provisioned \|**

**What type of volume path \[7\]:**

**2020-11-07 15:00:12,223 - gluu-prompt-volumes - INFO - GCE GKE Options
(\'pd-standard\', \'pd-ssd\')**

**2020-11-07 15:00:12,224 - gluu-prompt-volumes - INFO - AWS EKS Options
(\'gp2\', \'io1\', \'st1\', \'sc1\')**

**2020-11-07 15:00:12,224 - gluu-prompt-volumes - INFO - Azure Options
(\'Standard_LRS\', \'Premium_LRS\', \'StandardSSD_LRS\',
\'UltraSSD_LRS\')**

**Please enter the volume type. \[io1\]: gp2**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| Is this a multi-cloud/region setup\[N\] ? \[Y/N\] \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| Notes \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**If you are planning for a multi-cloud/region setup and this is the
first cluster answer N or leave blank. You will answer Y for the second
and more cluster setup**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**Is this a multi-cloud/region setup \[N\] \[y/N\]:**

**Please input couchbase backup cron job schedule for incremental
backups. This will run backup job every 30 mins by default. \[\*/30 \*
\* \* \*\]:**

**Please input couchbase backup cron job schedule for full backups. This
will run backup job on Saturday at 2am \[0 2 \* \* 6\]:**

**Please enter the time period in which to retain existing backups.
Older backups outside this time frame are deleted \[168h\]:**

**Size of couchbase backup volume storage \[20Gi\]:**

**2020-11-07 15:00:35,051 - gluu-prompt-couchbase - INFO - For the
following prompt if placed \[N\] the couchbase is assumed to be
installed or remotely provisioned**

**Install Couchbase \[Y\] \[Y/n\]:**

**Override couchbase-cluster.yaml with a custom couchbase-cluster.yaml
\[N\] \[y/N\]:**

**Setup CB nodes using low resources for demo purposes \[N\] \[y/N\]:
y**

**Please enter a namespace for CB objects. \[cbns\]:**

**Please enter a cluster name. \[cbgluu\]:**

**Please enter couchbase (remote or local) URL base name
\[cbgluu.cbns.svc.cluster.local\]:**

**Please enter couchbase superuser username. \[admin\]:**

**Couchbase superuser password \[h\*\*\*}\`\]:**

**Confirm password:**

**2020-11-07 15:01:32,446 - gluu-common - INFO - Success! Couchbase
superuser password was set.**

**Please enter gluu couchbase username. \[gluu\]:**

**Couchbase Gluu user password \[3\*\*\*\^\|\]:**

**Confirm password:**

**2020-11-07 15:01:56,160 - gluu-common - INFO - Success! Couchbase Gluu
user password was set.**

**Enter Couchbase certificate common name. \[Couchbase CA\]:**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| Cache layer \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**\| \[1\] NATIVE_PERSISTENCE \[default\] \|**

**\| \[2\] IN_MEMORY \|**

**\| \[3\] REDIS \|**

**\|\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--\|**

**Cache layer \[1\]:**

**Enter Hostname \[demoexample.gluu.org\]: execute.centroxy.com**

**Enter Country Code \[US\]: IN**

**Enter State \[TX\]: OD**

**Enter City \[Austin\]: BBI**

**Enter email \[support\@gluu.org\]: sthita\@centroxy.com**

**Enter Organization \[Gluu\]: Centroxy**

**oxTrust password \[{\*\*\*\*1\]:**

**Confirm password:**

**2020-11-07 15:02:50,351 - gluu-common - INFO - Success! oxTrust
password was set.**

**Are you using a globally resolvable FQDN \[N\] \[y/N\]: y**

**2020-11-07 15:03:00,127 - gluu-prompt-config - INFO - You can mount
your FQDN certification and key by placing them inside gluu.crt and
gluu.key respectivley at the same location pygluu-kubernetes.pyz is
at.**

**2020-11-07 15:03:00,128 - gluu-prompt-config - WARNING - Main
configuration settings has been outputted to file:
./config/base/generate.json. Please store this file safely or delete
it.**

**Would you like to manually edit the image source/name and tag \[N\]
\[y/N\]:**

**Number of oxAuth replicas \[1\]:**

**Number of oxTrust replicas \[1\]:**

**Number of oxd-server replicas \[1\]:**

**Number of Casa replicas \[1\]:**

**\| Setting \| Value \|**

**\| ACCEPT_GLUU_LICENSE \| Y \|**

**\| GLUU_VERSION \| 4.2 \|**

**\| TEST_ENVIRONMENT \| N \|**

**\| GLUU_UPGRADE_TARGET_VERSION \| \|**

**\| GLUU_HELM_RELEASE_NAME \| \|**

**\| NGINX_INGRESS_RELEASE_NAME \| \|**

**\| NGINX_INGRESS_NAMESPACE \| \|**

**\| INSTALL_GLUU_GATEWAY \| Y \|**

**\| POSTGRES_NAMESPACE \| postgres \|**

**\| KONG_NAMESPACE \| gluu-gateway \|**

**\| GLUU_GATEWAY_UI_NAMESPACE \| gg-ui \|**

**\| KONG_PG_USER \| kong \|**

**\| GLUU_GATEWAY_UI_PG_USER \| konga \|**

**\| KONG_DATABASE \| kong \|**

**\| GLUU_GATEWAY_UI_DATABASE \| konga \|**

**\| POSTGRES_REPLICAS \| 3 \|**

**\| POSTGRES_URL \| postgres.postgres.svc.cluster.local \|**

**\| KONG_HELM_RELEASE_NAME \| \|**

**\| GLUU_GATEWAY_UI_HELM_RELEASE_NAME \| \|**

**\| USE_ISTIO \| N \|**

**\| USE_ISTIO_INGRESS \| N \|**

**\| ISTIO_SYSTEM_NAMESPACE \| \|**

**\| NODE_SSH_KEY \| \~/.ssh/id_rsa \|**

**\| HOST_EXT_IP \| 22.22.22.22 \|**

**\| VERIFY_EXT_IP \| \|**

**\| AWS_LB_TYPE \| clb \|**

**\| USE_ARN \| N \|**

**\| VPC_CIDR \| \|**

**\| ARN_AWS_IAM \| \|**

**\| LB_ADD \| \|**

**\| REDIS_URL \| \|**

**\| REDIS_TYPE \| \|**

**\| REDIS_USE_SSL \| false \|**

**\| REDIS_SSL_TRUSTSTORE \| \|**

**\| REDIS_SENTINEL_GROUP \| \|**

**\| REDIS_MASTER_NODES \| \|**

**\| REDIS_NODES_PER_MASTER \| \|**

**\| REDIS_NAMESPACE \| \|**

**\| INSTALL_REDIS \| \|**

**\| INSTALL_JACKRABBIT \| Y \|**

**\| JACKRABBIT_STORAGE_SIZE \| 4Gi \|**

**\| JACKRABBIT_URL \| http://jackrabbit:8080 \|**

**\| JACKRABBIT_ADMIN_ID \| admin \|**

**\| JACKRABBIT_ADMIN_PASSWORD \| Centroxy\@123 \|**

**\| JACKRABBIT_CLUSTER \| Y \|**

**\| JACKRABBIT_PG_USER \| jackrabbit \|**

**\| JACKRABBIT_PG_PASSWORD \| Centroxy\@123 \|**

**\| JACKRABBIT_DATABASE \| jackrabbit \|**

**\| DEPLOYMENT_ARCH \| eks \|**

**\| PERSISTENCE_BACKEND \| couchbase \|**

**\| INSTALL_COUCHBASE \| Y \|**

**\| COUCHBASE_NAMESPACE \| cbns \|**

**\| COUCHBASE_VOLUME_TYPE \| \|**

**\| COUCHBASE_CLUSTER_NAME \| cbgluu \|**

**\| COUCHBASE_URL \| cbgluu.cbns.svc.cluster.local \|**

**\| COUCHBASE_USER \| gluu \|**

**\| COUCHBASE_SUPERUSER \| admin \|**

**\| COUCHBASE_SUPERUSER_PASSWORD \| Centroxy\@123 \|**

**\| COUCHBASE_CRT \| \|**

**\| COUCHBASE_CN \| Couchbase CA \|**

**\| COUCHBASE_CLUSTER_FILE_OVERRIDE \| N \|**

**\| COUCHBASE_USE_LOW_RESOURCES \| Y \|**

**\| COUCHBASE_DATA_NODES \| \|**

**\| COUCHBASE_QUERY_NODES \| \|**

**\| COUCHBASE_INDEX_NODES \| \|**

**\| COUCHBASE_SEARCH_EVENTING_ANALYTICS_NODES \| \|**

**\| COUCHBASE_GENERAL_STORAGE \| \|**

**\| COUCHBASE_DATA_STORAGE \| \|**

**\| COUCHBASE_INDEX_STORAGE \| \|**

**\| COUCHBASE_QUERY_STORAGE \| \|**

**\| COUCHBASE_ANALYTICS_STORAGE \| \|**

**\| COUCHBASE_INCR_BACKUP_SCHEDULE \| \*/30 \* \* \* \* \|**

**\| COUCHBASE_FULL_BACKUP_SCHEDULE \| 0 2 \* \* 6 \|**

**\| COUCHBASE_BACKUP_RETENTION_TIME \| 168h \|**

**\| COUCHBASE_BACKUP_STORAGE_SIZE \| 20Gi \|**

**\| LDAP_BACKUP_SCHEDULE \| \|**

**\| NUMBER_OF_EXPECTED_USERS \| \|**

**\| EXPECTED_TRANSACTIONS_PER_SEC \| \|**

**\| USING_CODE_FLOW \| \|**

**\| USING_SCIM_FLOW \| \|**

**\| USING_RESOURCE_OWNER_PASSWORD_CRED_GRANT_FLOW \| \|**

**\| DEPLOY_MULTI_CLUSTER \| N \|**

**\| HYBRID_LDAP_HELD_DATA \| \|**

**\| LDAP_JACKRABBIT_VOLUME \| gp2 \|**

**\| APP_VOLUME_TYPE \| 7 \|**

**\| LDAP_STATIC_VOLUME_ID \| \|**

**\| LDAP_STATIC_DISK_URI \| \|**

**\| GLUU_CACHE_TYPE \| NATIVE_PERSISTENCE \|**

**\| GLUU_NAMESPACE \| gluu \|**

**\| GLUU_FQDN \| execute.centroxy.com \|**

**\| COUNTRY_CODE \| IN \|**

**\| STATE \| OD \|**

**\| EMAIL \| sthita\@centroxy.com \|**

**\| CITY \| BBI \|**

**\| ORG_NAME \| Centroxy \|**

**\| GMAIL_ACCOUNT \| \|**

**\| GOOGLE_NODE_HOME_DIR \| \|**

**\| IS_GLUU_FQDN_REGISTERED \| Y \|**

**\| OXD_APPLICATION_KEYSTORE_CN \| oxd-server \|**

**\| OXD_ADMIN_KEYSTORE_CN \| oxd-server \|**

**\| LDAP_STORAGE_SIZE \| \|**

**\| OXAUTH_REPLICAS \| 1 \|**

**\| OXTRUST_REPLICAS \| 1 \|**

**\| LDAP_REPLICAS \| \|**

**\| OXSHIBBOLETH_REPLICAS \| \|**

**\| OXPASSPORT_REPLICAS \| \|**

**\| OXD_SERVER_REPLICAS \| 1 \|**

**\| CASA_REPLICAS \| 1 \|**

**\| RADIUS_REPLICAS \| \|**

**\| FIDO2_REPLICAS \| \|**

**\| SCIM_REPLICAS \| \|**

**\| ENABLE_OXTRUST_API \| N \|**

**\| ENABLE_OXTRUST_TEST_MODE \| N \|**

**\| ENABLE_CACHE_REFRESH \| N \|**

**\| ENABLE_OXD \| Y \|**

**\| ENABLE_FIDO2 \| N \|**

**\| ENABLE_SCIM \| N \|**

**\| ENABLE_RADIUS \| N \|**

**\| ENABLE_OXPASSPORT \| N \|**

**\| ENABLE_OXSHIBBOLETH \| N \|**

**\| ENABLE_CASA \| Y \|**

**\| ENABLE_OXAUTH_KEY_ROTATE \| N \|**

**\| ENABLE_OXTRUST_API_BOOLEAN \| true \|**

**\| ENABLE_OXTRUST_TEST_MODE_BOOLEAN \| false \|**

**\| ENABLE_RADIUS_BOOLEAN \| false \|**

**\| ENABLE_OXPASSPORT_BOOLEAN \| false \|**

**\| ENABLE_CASA_BOOLEAN \| true \|**

**\| ENABLE_SAML_BOOLEAN \| false \|**

**\| ENABLED_SERVICES_LIST \| persistence, jackrabbit, oxtrust,
gluu-gateway-ui, oxd-server, oxauth, config, casa \|**

**\| OXAUTH_KEYS_LIFE \| \|**

**\| EDIT_IMAGE_NAMES_TAGS \| N \|**

**\| CASA_IMAGE_NAME \| gluufederation/casa \|**

**\| CASA_IMAGE_TAG \| 4.2.1_02 \|**

**\| CONFIG_IMAGE_NAME \| gluufederation/config-init \|**

**\| CONFIG_IMAGE_TAG \| 4.2.1_02 \|**

**\| CACHE_REFRESH_ROTATE_IMAGE_NAME \| gluufederation/cr-rotate \|**

**\| CACHE_REFRESH_ROTATE_IMAGE_TAG \| 4.2.1_02 \|**

**\| CERT_MANAGER_IMAGE_NAME \| gluufederation/certmanager \|**

**\| CERT_MANAGER_IMAGE_TAG \| 4.2.1_02 \|**

**\| LDAP_IMAGE_NAME \| gluufederation/opendj \|**

**\| LDAP_IMAGE_TAG \| 4.2.1_02 \|**

**\| JACKRABBIT_IMAGE_NAME \| gluufederation/jackrabbit \|**

**\| JACKRABBIT_IMAGE_TAG \| 4.2.1_02 \|**

**\| OXAUTH_IMAGE_NAME \| gluufederation/oxauth \|**

**\| OXAUTH_IMAGE_TAG \| 4.2.1_02 \|**

**\| FIDO2_IMAGE_NAME \| gluufederation/fido2 \|**

**\| FIDO2_IMAGE_TAG \| 4.2.1_02 \|**

**\| SCIM_IMAGE_NAME \| gluufederation/scim \|**

**\| SCIM_IMAGE_TAG \| 4.2.1_04 \|**

**\| OXD_IMAGE_NAME \| gluufederation/oxd-server \|**

**\| OXD_IMAGE_TAG \| 4.2.1_02 \|**

**\| OXPASSPORT_IMAGE_NAME \| gluufederation/oxpassport \|**

**\| OXPASSPORT_IMAGE_TAG \| 4.2.1_03 \|**

**\| OXSHIBBOLETH_IMAGE_NAME \| gluufederation/oxshibboleth \|**

**\| OXSHIBBOLETH_IMAGE_TAG \| 4.2.1_02 \|**

**\| OXTRUST_IMAGE_NAME \| gluufederation/oxtrust \|**

**\| OXTRUST_IMAGE_TAG \| 4.2.1_02 \|**

**\| PERSISTENCE_IMAGE_NAME \| gluufederation/persistence \|**

**\| PERSISTENCE_IMAGE_TAG \| 4.2.1_02 \|**

**\| RADIUS_IMAGE_NAME \| gluufederation/radius \|**

**\| RADIUS_IMAGE_TAG \| 4.2.1_02 \|**

**\| GLUU_GATEWAY_IMAGE_NAME \| gluufederation/gluu-gateway \|**

**\| GLUU_GATEWAY_IMAGE_TAG \| 4.2.1_03 \|**

**\| GLUU_GATEWAY_UI_IMAGE_NAME \| gluufederation/gluu-gateway-ui \|**

**\| GLUU_GATEWAY_UI_IMAGE_TAG \| 4.2.1_02 \|**

**\| UPGRADE_IMAGE_NAME \| gluufederation/upgrade \|**

**\| UPGRADE_IMAGE_TAG \| 4.2.1_04 \|**

**\| CONFIRM_PARAMS \| N \|**

**Please confirm the above settings \[y/N\]: y**

After Complete Installation check all pods are up and running in gluu,
cbns, ingress-nginx, gluu-gateway & gg-ui namespaces:

**\[root\@ip-192-168-118-218 /\]\# kubectl get pod -n gluu**

![](media/image1.png){width="6.243478783902012in"
height="1.5384109798775154in"}

To accesss couchbase-ui port-forward the couchbase pod in cbns
namespace.

**\[root\@ip-192-168-118-218 /\]\# kubectl get pod -n cbns**

![](media/image2.png){width="6.5in" height="0.6027777777777777in"}

**kubectl port-forward \<pod-name\> -n cbns 8091 \--address 0.0.0.0**

To access gluu-ui, map gluu host-name (execute.centroxy.com) with
ingress-nginx external-ip.

**\[root\@ip-192-168-118-218 /\]\# kubectl get all --n ingress-nginx**

![](media/image3.png){width="6.49747375328084in"
height="1.0339370078740158in"}

Map gateway host-name (k8gg42.centroxy.com) with kong-proxy

external-ip in host file & use kong-admin external ip as kong-api-url.

**\[root\@ip-192-168-118-218 /\]\# kubectl get all --n gluu-gateway**

![](media/image4.png){width="6.582608267716536in"
height="1.7398906386701662in"}

Use gg-kong-ui loadBalancer-ip in gg-ui namespace to access
gluu-gateway-ui:

**\[root\@ip-192-168-118-218 /\]\# kubectl get all -n gg-ui**

![](media/image5.png){width="6.139130577427822in"
height="1.2593088363954505in"}
