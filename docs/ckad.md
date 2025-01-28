# CKAD

# Configuration

# 001 - Define, build and modify container images

### How to create my own image?

Ejemplo:

Crear una imagen para una aplicacion web sencilla

1\. Anotar los pasos del proceso de como se haria manualmente.

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/sq5image.png)](http://10.10.56.89/uploads/images/gallery/2025-01/sq5image.png)

2\. Crear el archivo Dockerfile con las instrucciones

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/SuWimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/SuWimage.png)

3\. Crear la imagen con el comando de compilacion de Docker

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/DS1image.png)](http://10.10.56.89/uploads/images/gallery/2025-01/DS1image.png)

4\. Subir la imagen a dockerfile para que sea publica

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/AJEimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/AJEimage.png)

Dockerfile

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/xiOimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/xiOimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/9UNimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/9UNimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/UU5image.png)](http://10.10.56.89/uploads/images/gallery/2025-01/UU5image.png)

Layered architecture

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/5Zmimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/5Zmimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/NWCimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/NWCimage.png)

Docker build output

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/gN4image.png)](http://10.10.56.89/uploads/images/gallery/2025-01/gN4image.png)

failure

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/Kakimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/Kakimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/KCBimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/KCBimage.png)

# 002 - Commands

docker build -t webapp-color .

# 003 - Commands and Arguments in Docker

- `docker run ubuntu`: Crea y ejecuta un contenedor con la imagen `ubuntu`.
- `docker ps`: Muestra los contenedores activos en ejecución.
- `docker ps -a`: Lista todos los contenedores, incluidos los detenidos.
- `docker run ubuntu [COMMAND]`: Ejecuta un contenedor basado en `ubuntu` con el comando especificado.
- `docker run ubuntu sleep 5`: Inicia un contenedor con `ubuntu` y ejecuta el comando `sleep 5` (espera 5 segundos).
- `docker build -t ubuntu-sleeper .`: Construye una imagen llamada `ubuntu-sleeper` a partir del Dockerfile en el directorio actual.
- `docker run ubuntu-sleeper`: Ejecuta un contenedor basado en la imagen `ubuntu-sleeper`.

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/Ogdimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/Ogdimage.png)

docker run ubuntu-sleeper sleep 10

docker run ubuntu-sleeper 10

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/rq5image.png)](http://10.10.56.89/uploads/images/gallery/2025-01/rq5image.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/WpLimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/WpLimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/gGbimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/gGbimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/3OZimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/3OZimage.png)

# 004 -  Commands and Arguments in Kubernetes

docker run --name ubuntu-sleeper ubuntu-sleeper

docker run --name ubuntu-sleeper ubuntu sleeper 10

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/EeVimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/EeVimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/Ckuimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/Ckuimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/H73image.png)](http://10.10.56.89/uploads/images/gallery/2025-01/H73image.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/U5Wimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/U5Wimage.png)

# 005 - A quick note on editing Pods and Deployments

<div class="ud-heading-xxl text-viewer--main-heading--pPafb" id="bkmrk-a-quick-note-on-edit">A quick note on editing Pods and Deployments</div>#### Edit a POD

Remember, you CANNOT edit specifications of an existing POD other than the below.

<div class="article-asset--container--IvjZK" id="bkmrk-spec.containers%5B%2A%5D.i"><div class="article-asset--content--H92b2 rt-scaffolding" data-purpose="safely-set-inner-html:rich-text-viewer:html">- spec.containers\[\*\].image
- spec.initContainers\[\*\].image
- spec.activeDeadlineSeconds
- spec.tolerations

</div></div>For example you cannot edit the environment variables, service accounts, resource limits (all of which we will discuss later) of a running pod. But if you really want to, you have 2 options:

1\. Run the `kubectl edit pod <pod name>` command. This will open the pod specification in an editor (vi editor). Then edit the required properties. When you try to save it, you will be denied. This is because you are attempting to edit a field on the pod that is not editable.

<div class="article-asset--container--IvjZK" id="bkmrk-"><div class="article-asset--content--H92b2 rt-scaffolding" data-purpose="safely-set-inner-html:rich-text-viewer:html"><figure>![](https://img-c.udemycdn.com/redactor/raw/2019-05-30_14-46-21-89ea56fea6b993ee0ccff1625b13341e.PNG)</figure><figure>![](https://img-c.udemycdn.com/redactor/raw/2019-05-30_14-47-14-07b2638d1a72cb2d5b000c00971f6436.PNG)</figure></div></div>A copy of the file with your changes is saved in a temporary location as shown above.

You can then delete the existing pod by running the command:

`kubectl delete pod webapp`

Then create a new pod with your changes using the temporary file

`kubectl create -f /tmp/kubectl-edit-ccvrq.yaml`

2\. The second option is to extract the pod definition in YAML format to a file using the command

`kubectl get pod webapp -o yaml > my-new-pod.yaml`

Then make the changes to the exported file using an editor (vi editor). Save the changes

`vi my-new-pod.yaml`

Then delete the existing pod

`kubectl delete pod webapp`

Then create a new pod with the edited file

`kubectl create -f my-new-pod.yaml`

#### Edit Deployments

With Deployments you can easily edit any field/property of the POD template. Since the pod template is a child of the deployment specification, with every change the deployment will automatically delete and create a new pod with the new changes. So if you are asked to edit a property of a POD part of a deployment you may do that simply by running the command

`kubectl edit deployment my-deployment`

# 006 - Environment Variables

En Kubernetes, las **Environment Variables** son configuraciones que puedes pasar a los contenedores para personalizar su comportamiento. Se definen en el manifiesto del pod o Deployment bajo la sección `env`.

Estas variables pueden tener valores fijos o dinámicos, obtenidos de ConfigMaps o Secrets, y son útiles para almacenar configuraciones como credenciales o URLs sin codificarlas directamente.

Ejemplo de configuración:

<div class="flex max-w-full flex-col flex-grow" id="bkmrk-"><div class="min-h-8 text-message flex w-full flex-col items-end gap-2 whitespace-normal break-words text-start [.text-message+&]:mt-5" data-message-author-role="assistant" data-message-id="f345b3d0-84c1-4964-ad19-6e4de8dabfe5" data-message-model-slug="gpt-4o" dir="auto"><div class="flex w-full flex-col gap-1 empty:hidden first:pt-[3px]"><div class="markdown prose w-full break-words dark:prose-invert light"><div class="contain-inline-size rounded-md border-[0.5px] border-token-border-medium relative bg-token-sidebar-surface-primary dark:bg-gray-950"></div></div></div></div></div>```yaml
env:
- name: APP_ENV
  value: production
- name: DATABASE_URL
  valueFrom:
    secretKeyRef:
      name: db-secret
      key: url
```

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/zwUimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/zwUimage.png)

En Kubernetes, los valores de las **Environment Variables** pueden definirse de tres formas principales:

- **Valores fijos**: Se especifican directamente en el manifiesto.

```yaml
env:
- name: APP_ENV
  value: production
```

- **Valores dinámicos desde ConfigMaps o Secrets**: Se obtienen de estos objetos para gestionar configuraciones sensibles o centralizadas

```yaml
env:
- name: DATABASE_URL
  valueFrom:
    configMapKeyRef:
      name: app-config
      key: database_url
```

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/gREimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/gREimage.png)

# 007 - ConfigMaps

Un **ConfigMap** en Kubernetes es un objeto utilizado para almacenar datos de configuración no sensibles en pares clave-valor. Permite desacoplar la configuración del código de la aplicación, haciendo que sea más fácil modificar configuraciones sin necesidad de redeployar.

Los ConfigMaps pueden ser referenciados en pods como variables de entorno, archivos montados en volúmenes o argumentos del contenedor. Esto los hace ideales para gestionar configuraciones como URLs, nombres de servidores y parámetros de aplicaciones.

##### Imperative

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/YDfimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/YDfimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/FbSimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/FbSimage.png)

##### Declarative

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/YbIimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/YbIimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/m7Qimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/m7Qimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/PMQimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/PMQimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/LLhimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/LLhimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/fKHimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/fKHimage.png)

# Core Concepts

# 001 - Recap - Kubernetes Architecture

## Node:

Un **Node** en Kubernetes es una máquina (física o virtual) que ejecuta los pods, proporcionando los recursos de CPU, memoria, red y almacenamiento necesarios. Cada Node tiene un agente kubelet que comunica su estado con el clúster y administra los contenedores

## Cluster:

Un **Cluster** en Kubernetes es un conjunto de nodos (máquinas) que trabajan juntos para ejecutar aplicaciones en contenedores. Está compuesto por un **control plane** que gestiona el estado del clúster y los **nodes** que ejecutan los workloads

## Master:

El **Master** en Kubernetes (o Control Plane) es el componente central que administra el clúster, coordinando las actividades de los nodos. Incluye el **API Server**, **Scheduler**, **Controller Manager** y **etcd** para gestionar el estado y la configuración del clúster.<span class="" data-state="closed"><button aria-expanded="false" aria-haspopup="menu" class="cursor-pointer h-[30px] rounded-md px-1 text-token-text-secondary hover:bg-token-main-surface-secondary" data-state="closed" id="bkmrk-" type="button"></button></span>

## Componentes:

Los componentes principales de Kubernetes son:

1. **Control Plane**:
    
    
    - **API Server**: Gestiona la comunicación entre los usuarios y el clúster.
    - **etcd**: Almacén clave-valor para el estado del clúster.
    - **Scheduler**: Asigna pods a nodos según recursos y políticas.
    - **Controller Manager**: Gestiona controladores, como replicación y endpoints.
2. **Node Components**:
    
    
    - **Kubelet**: Agente que asegura que los contenedores estén en ejecución.
    - **Kube-proxy**: Gestiona la red y el acceso a los servicios.
    - **Container Runtime**: Ejecuta contenedores (e.g., Docker, containerd).

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/V9Dimage.png)](http://10.10.56.89/uploads/images/gallery/2024-12/V9Dimage.png)

## Master vs Worker Nodes

### **Master Node (Control Plane):**

- Administra el clúster y toma decisiones como programar pods.
- Componentes clave: **API Server**, **etcd**, **Scheduler**, y **Controller Manager**.
- No ejecuta aplicaciones directamente (excepto en clústeres pequeños, como Minikube).

### **Worker Node:**

- Ejecuta los **pods** con las aplicaciones y cargas de trabajo.
- Componentes clave: **Kubelet**, **Kube-proxy**, y el **Container Runtime**.
- Recibe instrucciones del Master Node para ejecutar y gestionar los pods.

En resumen, el Master coordina y los Worker Nodes ejecutan.

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/eP0image.png)](http://10.10.56.89/uploads/images/gallery/2024-12/eP0image.png)

## Kubectl

**`kubectl`** es la herramienta de línea de comandos para interactuar con un clúster de Kubernetes. Permite gestionar recursos como pods, servicios, y deployments, así como monitorear el estado del clúster y ejecutar comandos en los contenedores.

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/lndimage.png)](http://10.10.56.89/uploads/images/gallery/2024-12/lndimage.png)

# 002 - Docker-vs-ContainerD

### **Docker**:

- **Descripción**: Docker es una plataforma completa que facilita la creación, envío y ejecución de contenedores. Incluye un conjunto de herramientas como el **Docker Engine**, **Docker Compose**, y **Docker Hub**.
- **Uso**: Además de ejecutar contenedores, también gestiona la construcción de imágenes y la orquestación con Docker Swarm.

### **containerd**:

- **Descripción**: containerd es un runtime de contenedores que proporciona las funcionalidades básicas necesarias para ejecutar contenedores, como la ejecución de contenedores, la gestión de imágenes y la administración del ciclo de vida de los contenedores. Es más ligero y especializado en la ejecución de contenedores, sin las herramientas adicionales que ofrece Docker.
- **Uso**: Usado por Kubernetes y otras plataformas de contenedores para gestionar la ejecución de contenedores.

### Diferencia clave:

- **Docker** es más una plataforma completa que gestiona todo el ciclo de vida de los contenedores, mientras que **containerd** se centra en la ejecución y gestión de contenedores, siendo más eficiente para proyectos específicos.

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/DYGimage.png)](http://10.10.56.89/uploads/images/gallery/2024-12/DYGimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/LCbimage.png)](http://10.10.56.89/uploads/images/gallery/2024-12/LCbimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/hdUimage.png)](http://10.10.56.89/uploads/images/gallery/2024-12/hdUimage.png)

# 003 - Recap - Pods

## POD

Un **Pod** en Kubernetes es la unidad básica de despliegue que puede contener uno o más contenedores (típicamente en el mismo host). Los contenedores dentro de un pod comparten el mismo almacenamiento, red y especificaciones, lo que permite una estrecha comunicación y gestión eficiente. Los pods son efímeros y gestionados por el control plane de Kubernetes.

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/BMZimage.png)](http://10.10.56.89/uploads/images/gallery/2024-12/BMZimage.png)

## **Multi-Container Pod**

Un **Multi-Container Pod** en Kubernetes es un pod que contiene más de un contenedor. Estos contenedores comparten red, almacenamiento y contexto, permitiendo una comunicación eficiente. Se usan para patrones como:

- **Sidecar**: Un contenedor complementa al principal, como un proxy o logger.
- **Adapter**: Transforma datos para otro contenedor en el mismo pod.
- **Ambassador**: Maneja la comunicación con servicios externos.

Todos los contenedores trabajan como una unidad cohesiva para cumplir un objetivo común.

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/gogimage.png)](http://10.10.56.89/uploads/images/gallery/2024-12/gogimage.png)

## Kubectl

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/7dBimage.png)](http://10.10.56.89/uploads/images/gallery/2024-12/7dBimage.png)

# 004 - Pods with YAML

## YAML

**YAML (Yet Another Markup Language)** es un formato de texto legible para humanos usado en Kubernetes para definir recursos del clúster. Es jerárquico y utiliza espacios para estructurar datos en clave-valor.

### Cuatro campos de nivel superior

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/Tsbimage.png)](http://10.10.56.89/uploads/images/gallery/2024-12/Tsbimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/pumimage.png)](http://10.10.56.89/uploads/images/gallery/2024-12/pumimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/bIRimage.png)](http://10.10.56.89/uploads/images/gallery/2024-12/bIRimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/iKqimage.png)](http://10.10.56.89/uploads/images/gallery/2024-12/iKqimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/oT0image.png)](http://10.10.56.89/uploads/images/gallery/2024-12/oT0image.png)

## Comandos

[![image.png](http://10.10.56.89/uploads/images/gallery/2024-12/scaled-1680-/u9dimage.png)](http://10.10.56.89/uploads/images/gallery/2024-12/u9dimage.png)

```yaml
kubectl run redis --image=redis123 --dry-run=client -o yaml
```

<span class="hljs-attr">  
</span>

# 005 - Creating Pod with YAML

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: myapp-pod
  labels:
    app: myapp
    costcenter: amer
    location: MX
spec:
  containers:
    - name: nginx-container
      image: nginx
```

# 006 - Edit PODS

## Edit Pods

#### A Note on Editing Existing Pods

In any of the practical quizzes, if you are asked to **edit an existing POD**, please note the following:

<div class="article-asset--container--IvjZK" id="bkmrk-if-you-are-given-a-p"><div class="article-asset--content--H92b2 rt-scaffolding" data-purpose="safely-set-inner-html:rich-text-viewer:html">- If you are given a pod definition file, edit that file and use it to create a new pod.
- **If you are not given a pod definition file**, you may extract the definition to a file using the below command:
    
    `kubectl get pod <pod-name> -o yaml > pod-definition.yaml`
    
    Then edit the file to make the necessary changes, delete, and re-create the pod.
- To modify the properties of the pod, you can utilize the `kubectl edit pod <pod-name> `command. Please note that only the properties listed below are editable.
    
    
    - spec.containers\[\*\].image
    - spec.initContainers\[\*\].image
    - spec.activeDeadlineSeconds
    - spec.tolerations
    - spec.terminationGracePeriodSeconds

</div></div>

# 007 - Replicasets

Replica

Una **réplica** en Kubernetes es una instancia de un pod que forma parte de un ReplicaSet o Deployment. Su propósito es garantizar alta disponibilidad y escalabilidad al duplicar aplicaciones en varios nodos.

El número de réplicas se define en el campo `replicas` en el manifiesto YAML del recurso. Por ejemplo, con `replicas: 3`, Kubernetes mantiene siempre tres pods activos.

ccReplicaset

Un **ReplicaSet** en Kubernetes asegura que un número específico de réplicas de un pod estén siempre corriendo en el clúster. Si un pod falla o es eliminado, el ReplicaSet lo reemplaza automáticamente.

Replicaset Controller

El **ReplicaSet Controller** es un controlador en Kubernetes que gestiona los recursos **ReplicaSet**. Su función principal es garantizar que el número deseado de réplicas de un pod esté siempre en ejecución en el clúster.

### Funciones clave del ReplicaSet Controller:

1. **Mantener el número de réplicas:** Si un pod falla o se elimina, crea uno nuevo para cumplir con el número especificado en `replicas`.
2. **Autoescalado:** Permite aumentar o disminuir manualmente el número de réplicas según las necesidades.
3. **Reconciliación:** Compara constantemente el estado actual del clúster con el estado deseado y actúa para mantenerlos alineados.

Crear Replicacion Controller

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/image.png)](http://10.10.56.89/uploads/images/gallery/2025-01/image.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/0Rqimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/0Rqimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/7MNimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/7MNimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/5SKimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/5SKimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/8D6image.png)](http://10.10.56.89/uploads/images/gallery/2025-01/8D6image.png)

<details id="bkmrk-rc-definition.yml-ap"><summary>rc-definition.yml</summary>

```yaml
apiVersion: v1
kind: ReplicationController
metadata:
  name: myapp-rc
  labels:
    app: myapp
    type: front-end
spec:
  template:
    metadata:
      name: myapp-pod
      labels:
        app: myapp
        type: front-end
    spec:
      containers:
      - name: nginx-container
        image: nginx
  replicas: 2
```

</details>```bash
kubectl create -f rc-definition.yml
```

```bash
kubectl get replicationcontroller  
```

Crear ReplicaSet

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/5taimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/5taimage.png)

<details id="bkmrk-replicaset-definitio"><summary>replicaset-definition.yml</summary>

```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: myapp-replicaset
  labels:
    app: myapp
    type: front-end
spec:
  template:
    metadata:
      name: myapp-pod
      labels:
        app: myapp
        type: front-end
    spec:
      containers:
      - name: nginx-container
        image: nginx
  replicas: 3
  selector:
    matchLabels:
      type: front-end
```

</details>```bash
kubectl create -f replicaset-definition.yml
```

```bash
kubectl get replicaset
```

Labels and Selectors

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/czRimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/czRimage.png)

Scale

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/i4Zimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/i4Zimage.png)

```bash
kubectl replace -f replicaset-definition.yml
```

```yaml
kubectl scale --replicas=7 -f replicaset-definition.yml
```

```bash
kubectl scale --replicas=8 replicaset myapp-replicaset 
```

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/wLQimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/wLQimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/1KKimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/1KKimage.png)

# 008 - Deployments

### Deployment

Un **Deployment** en Kubernetes es un recurso que administra la creación y el escalado de pods, asegurando que siempre cumplan con el estado deseado. Facilita las actualizaciones y escalabilidad de aplicaciones.

Permite implementar estrategias como actualizaciones progresivas (rolling updates) y revertir cambios si algo falla. Es ideal para gestionar aplicaciones de forma declarativa y mantener alta disponibilidad.

#### Rolling updates

Las **rolling updates** en Kubernetes son una estrategia para actualizar aplicaciones sin interrupciones. Kubernetes reemplaza gradualmente los pods antiguos por nuevos, asegurando que la aplicación permanezca disponible durante el proceso.

Se controla el número de pods que se crean o eliminan simultáneamente usando los parámetros `maxUnavailable` y `maxSurge` en el Deployment. Esto permite realizar actualizaciones de forma segura y progresiva.

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/tUzimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/tUzimage.png)

### Definition

Un **Deployment** en Kubernetes está compuesto por los siguientes elementos clave:

1. **Metadata**: Incluye información como el nombre del Deployment y etiquetas que ayudan a identificar recursos asociados.
2. **Spec (Especificación)**: Define el estado deseado, incluyendo el número de réplicas, el selector de pods, y la plantilla del pod (contenedores, imágenes y configuraciones).
3. **Selector**: Identifica los pods gestionados por el Deployment basándose en etiquetas.

<details id="bkmrk-deployment-definitio"><summary>deployment-definition.yaml</summary>

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: myapp-replicaset
  labels:
    app: myapp
    type: front-end
spec:
  template:
    metadata:
      name: myapp-pod
      labels:
        app: myapp
        type: front-end
    spec:
      containers:
      - name: nginx-container
        image: nginx
  replicas: 6
  selector:
    matchLabels:
      type: front-end
```

</details>```
kubectl create -f deployment-definition.yaml
```

```
kubectl get deployments
```

```
kubectl get replicaset
```

```
kubectl get pods
```

```
kubectl get all
```

# 009 - Certification Tip: Formatting Output with kubectl

The default output format for all **kubectl** commands is the human-readable plain-text format.

The -o flag allows us to output the details in several different formats.

**kubectl \[command\] \[TYPE\] \[NAME\] -o &lt;output\_format&gt;**

Here are some of the commonly used formats:

1. `-o json`Output a JSON formatted API object.
2. `-o name`Print only the resource name and nothing else.
3. `-o wide`Output in the plain-text format with any additional information.
4. `-o yaml`Output a YAML formatted API object.

Here are some useful examples:

- **Output with JSON format:**

```json
master $ kubectl create namespace test-123 --dry-run -o json
{
    "kind": "Namespace",
    "apiVersion": "v1",
    "metadata": {
        "name": "test-123",
        "creationTimestamp": null
    },
    "spec": {},
    "status": {}
}
master $
```

- **Output with YAML format:**

```yaml
master $ kubectl create namespace test-123 --dry-run -o yaml
apiVersion: v1
kind: Namespace
metadata:
  creationTimestamp: null
  name: test-123
spec: {}
status: {}
```

<div class="ud-component--base-components--code-block" id="bkmrk-"></div>- **Output with wide (additional details):**

Probably the most common format used to print additional details about the object:

```
master $ kubectl get pods -o wide
NAME      READY   STATUS    RESTARTS   AGE     IP          NODE     NOMINATED NODE   READINESS GATES
busybox   1/1     Running   0          3m39s   10.36.0.2   node01   <none>           <none>
ningx     1/1     Running   0          7m32s   10.44.0.1   node03   <none>           <none>
redis     1/1     Running   0          3m59s   10.36.0.1   node01   <none>           <none>
master $
```

<div class="ud-component--base-components--code-block" id="bkmrk--1"><div></div></div>For more details, refer:

[**https://kubernetes.io/docs/reference/kubectl/overview/**](https://kubernetes.io/docs/reference/kubectl/overview/)

[**https://kubernetes.io/docs/reference/kubectl/cheatsheet**](https://kubernetes.io/docs/reference/kubectl/cheatsheet)**/**

# 010 - Namespaces

Un **namespace** en Kubernetes es un mecanismo lógico para dividir recursos dentro de un clúster. Ayuda a organizar y aislar aplicaciones, facilitando la gestión de múltiples equipos o entornos (como desarrollo, pruebas y producción) en un mismo clúster.

Los namespaces permiten que recursos con el mismo nombre coexistan en el clúster, siempre que pertenezcan a namespaces diferentes. Kubernetes incluye namespaces predeterminados como `default`, `kube-system` y `kube-public`.

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/9qqimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/9qqimage.png)

El aislamiento en **namespaces** de Kubernetes permite separar recursos y configuraciones entre diferentes espacios lógicos dentro del clúster. Esto asegura que las aplicaciones o servicios de un namespace no interfieran con los de otro.

Cada namespace tiene su propio conjunto de recursos, como pods, servicios y configuraciones, permitiendo un control granular de acceso mediante roles y políticas (`Role` y `RoleBinding`). Este enfoque es útil para gestionar múltiples equipos o entornos en un mismo clúster.

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/E8rimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/E8rimage.png)

n Kubernetes, los **namespaces** pueden tener límites de recursos definidos para controlar el consumo de CPU y memoria dentro de ellos. Esto se logra utilizando un objeto llamado `ResourceQuota`, que establece restricciones en el uso total de recursos en un namespace específico.

Por ejemplo, se puede limitar la cantidad total de memoria o CPU que los pods en un namespace pueden usar, evitando que una aplicación consuma más de lo asignado y afecte a otras aplicaciones en el clúster. Esto mejora la gestión de recursos y la estabilidad del sistema.

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/NgOimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/NgOimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/ZIdimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/ZIdimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/2MMimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/2MMimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/pZsimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/pZsimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/GQmimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/GQmimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/W5mimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/W5mimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/FFkimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/FFkimage.png)

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/o7Limage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/o7Limage.png)

Un **ResourceQuota** en Kubernetes es un objeto que impone límites en el uso total de recursos dentro de un namespace. Controla la cantidad de recursos como CPU, memoria, pods, servicios y almacenamiento que los usuarios o aplicaciones pueden consumir en ese namespace.

Se utiliza para evitar que un namespace consuma más recursos de los permitidos, asegurando una distribución justa en el clúster. Es especialmente útil en clústeres compartidos por múltiples equipos o aplicaciones.

[![image.png](http://10.10.56.89/uploads/images/gallery/2025-01/scaled-1680-/gkGimage.png)](http://10.10.56.89/uploads/images/gallery/2025-01/gkGimage.png)

# 011 - Certification Tip: Imperative Commands

While you would be working mostly the declarative way - using definition files, imperative commands can help in getting one-time tasks done quickly, as well as generate a definition template easily. This would help save a considerable amount of time during your exams.

Before we begin, familiarize yourself with the two options that can come in handy while working with the below commands:

`--dry-run`: By default, as soon as the command is run, the resource will be created. If you simply want to test your command, use the `--dry-run=client` option. This will not create the resource. Instead, tell you whether the resource can be created and if your command is right.

`-o yaml`: This will output the resource definition in YAML format on the screen.

Use the above two in combination along with Linux output redirection to generate a resource definition file quickly, that you can then modify and create resources as required, instead of creating the files from scratch.

`kubectl run nginx --image=nginx --dry-run=client -o yaml > nginx-pod.yaml`

#### POD

**Create an NGINX Pod**

`kubectl run nginx --image=nginx`

**Generate POD Manifest YAML file (-o yaml). Don't create it(--dry-run)**

`kubectl run nginx --image=nginx --dry-run=client -o yaml`

#### Deployment

**Create a deployment**

`kubectl create deployment --image=nginx nginx`

**Generate Deployment YAML file (-o yaml). Don't create it(--dry-run)**

`kubectl create deployment --image=nginx nginx --dry-run -o yaml`

**Generate Deployment with 4 Replicas**

`kubectl create deployment nginx --image=nginx --replicas=4`

You can also scale deployment using the `kubectl scale` command.

`kubectl scale deployment nginx --replicas=4`

**Another way to do this is to save the YAML definition to a file and modify**

kubectl create deployment nginx --image=nginx`--dry-run=client -o yaml > nginx-deployment.yaml`

You can then update the YAML file with the replicas or any other field before creating the deployment.

#### Service

**Create a Service named redis-service of type ClusterIP to expose pod redis on port 6379**

`kubectl expose pod redis --port=6379 --name redis-service --dry-run=client -o yaml`

(This will automatically use the pod's labels as selectors)

Or

`kubectl create service clusterip redis --tcp=6379:6379 --dry-run=client -o yaml` (This will not use the pods' labels as selectors; instead it will assume selectors as **app=redis.** [You cannot pass in selectors as an option.](https://github.com/kubernetes/kubernetes/issues/46191) So it does not work well if your pod has a different label set. So generate the file and modify the selectors before creating the service)

**Create a Service named nginx of type NodePort to expose pod nginx's port 80 on port 30080 on the nodes:**

`kubectl expose pod nginx --port=80 --name nginx-service --type=NodePort --dry-run=client -o yaml`

(This will automatically use the pod's labels as selectors, [but you cannot specify the node port](https://github.com/kubernetes/kubernetes/issues/25478). You have to generate a definition file and then add the node port in manually before creating the service with the pod.)

Or

`kubectl create service nodeport nginx --tcp=80:80 --node-port=30080 --dry-run=client -o yaml`

(This will not use the pods' labels as selectors)

Both the above commands have their own challenges. While one of it cannot accept a selector the other cannot accept a node port. I would recommend going with the `kubectl expose` command. If you need to specify a node port, generate a definition file using the same command and manually input the nodeport before creating the service.

**Reference:**

[https://kubernetes.io/docs/reference/kubectl/conventions/](https://kubernetes.io/docs/reference/kubectl/conventions/)

# Practice Test

# 001 - Pods

Create a new pod with the `nginx` image.

```bash
kubectl run nginx --image=nginx
```

Delete the `webapp` Pod.

```bash
kubectl delete pod webapp
```

Create a new pod with the name `redis` and the image `redis123`.

Metodo 1:

```bash
kubectl run redis --image=redis123 -o yaml
```

<details id="bkmrk-pod-definition.yaml-"><summary>pod-definition.yaml</summary>

```yaml
apiVersion: v1
kind: Pod
metadata:
  creationTimestamp: "2025-01-27T19:03:35Z"
  labels:
    run: redis
  name: redis
  namespace: default
  resourceVersion: "1059"
  uid: 74c5fb2d-9479-4d03-ba3b-509663a2245b
spec:
  containers:
  - image: redis123
    imagePullPolicy: Always
    name: redis
    resources: {}
    terminationMessagePath: /dev/termination-log
    terminationMessagePolicy: File
    volumeMounts:
    - mountPath: /var/run/secrets/kubernetes.io/serviceaccount
      name: kube-api-access-5k4xq
      readOnly: true
  dnsPolicy: ClusterFirst
  enableServiceLinks: true
  preemptionPolicy: PreemptLowerPriority
  priority: 0
  restartPolicy: Always
  schedulerName: default-scheduler
  securityContext: {}
  serviceAccount: default
  serviceAccountName: default
  terminationGracePeriodSeconds: 30
  tolerations:
  - effect: NoExecute
    key: node.kubernetes.io/not-ready
    operator: Exists
    tolerationSeconds: 300
  - effect: NoExecute
    key: node.kubernetes.io/unreachable
    operator: Exists
    tolerationSeconds: 300
  volumes:
  - name: kube-api-access-5k4xq
    projected:
      defaultMode: 420
      sources:
      - serviceAccountToken:
          expirationSeconds: 3607
          path: token
      - configMap:
          items:
          - key: ca.crt
            path: ca.crt
          name: kube-root-ca.crt
      - downwardAPI:
          items:
          - fieldRef:
              apiVersion: v1
              fieldPath: metadata.namespace
            path: namespace
status:
  phase: Pending
  qosClass: BestEffort
```

</details>Metodo 2:

<details id="bkmrk-pod-definition-v1.ya"><summary>pod-definition-v1.yaml</summary>

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: redis
spec:
  containers:
  - name: redis
    image: redis123
```

</details>

# 002 - Replicasets

Create a ReplicaSet using the `replicaset-definition-1.yaml` file located at `/root/`.

There is an issue with the file, so try to fix it.

<details id="bkmrk-issue-apiversion%3A-v1"><summary>Issue</summary>

```yaml
apiVersion: v1
kind: ReplicaSet
metadata:
  name: replicaset-1
spec:
  replicas: 2
  selector:
    matchLabels:
      tier: frontend
  template:
    metadata:
      labels:
        tier: frontend
    spec:
      containers:
      - name: nginx
        image: nginx
```

</details>```bash
kubectl api-resources | grep replicaset
```

<details id="bkmrk-fixed-apiversion%3A-ap"><summary>Fixed</summary>

```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: replicaset-1
spec:
  replicas: 2
  selector:
    matchLabels:
      tier: frontend
  template:
    metadata:
      labels:
        tier: frontend
    spec:
      containers:
      - name: nginx
        image: nginx
```

</details>Fix the issue in the `replicaset-definition-2.yaml` file and create a `ReplicaSet` using it.

This file is located at `/root/`.

<details id="bkmrk-issue-apiversion%3A-ap"><summary>Issue</summary>

```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: replicaset-2
spec:
  replicas: 2
  selector:
    matchLabels:
      tier: frontend
  template:
    metadata:
      labels:
        tier: nginx
    spec:
      containers:
      - name: nginx
        image: nginx
```

</details><details id="bkmrk-fixed-apiversion%3A-ap-1"><summary>Fixed</summary>

```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: replicaset-2
spec:
  replicas: 2
  selector:
    matchLabels:
      tier: nginx
  template:
    metadata:
      labels:
        tier: nginx
    spec:
      containers:
      - name: nginx
        image: nginx
```

</details>Fix the original replica set `new-replica-set` to use the correct `busybox` image.

Either delete and recreate the ReplicaSet or Update the existing ReplicaSet and then delete all PODs, so new ones with the correct image will be created.

```
kubectl edit replicaset new-replica-set 
```

<details id="bkmrk-issue-apiversion%3A-ap-1"><summary>Issue</summary>

```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  creationTimestamp: "2025-01-27T19:19:58Z"
  generation: 2
  name: new-replica-set
  namespace: default
  resourceVersion: "1593"
  uid: aed6557a-5462-4d6d-8e41-39216539f2f4
spec:
  replicas: 4
  selector:
    matchLabels:
      name: busybox-pod
  template:
    metadata:
      creationTimestamp: null
      labels:
        name: busybox-pod
    spec:
      containers:
      - command:
        - sh
        - -c
        - echo Hello Kubernetes! && sleep 3600
        image: busybox777
        imagePullPolicy: Always
        name: busybox-container
        resources: {}
        terminationMessagePath: /dev/termination-log
        terminationMessagePolicy: File
      dnsPolicy: ClusterFirst
      restartPolicy: Always
      schedulerName: default-scheduler
      securityContext: {}
      terminationGracePeriodSeconds: 30
status:
  fullyLabeledReplicas: 4
  observedGeneration: 2
  replicas: 4
```

</details><details id="bkmrk-fixed-apiversion%3A-ap-2"><summary>Fixed</summary>

```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  creationTimestamp: "2025-01-27T19:19:58Z"
  generation: 2
  name: new-replica-set
  namespace: default
  resourceVersion: "1593"
  uid: aed6557a-5462-4d6d-8e41-39216539f2f4
spec:
  replicas: 4
  selector:
    matchLabels:
      name: busybox-pod
  template:
    metadata:
      creationTimestamp: null
      labels:
        name: busybox-pod
    spec:
      containers:
      - command:
        - sh
        - -c
        - echo Hello Kubernetes! && sleep 3600
        image: busybox
        imagePullPolicy: Always
        name: busybox-container
        resources: {}
        terminationMessagePath: /dev/termination-log
        terminationMessagePolicy: File
      dnsPolicy: ClusterFirst
      restartPolicy: Always
      schedulerName: default-scheduler
      securityContext: {}
      terminationGracePeriodSeconds: 30
status:
  fullyLabeledReplicas: 4
  observedGeneration: 2
  replicas: 4
```

</details>```bash
kubectl delete pod new-replica-set-mr7mk  new-replica-set-rvlcc new-replica-set-vn9fs
```

Scale the ReplicaSet to 5 PODs.

Use `kubectl scale` command or edit the replicaset using `kubectl edit replicaset`.

Metodo Imperativo

```bash
kubectl scale --replicas=5 rs/new-replica-set
```

Metodo Declarativo

```bash
kubectl edit rs new-replica-set
```

```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  creationTimestamp: "2025-01-27T19:19:58Z"
  generation: 7
  name: new-replica-set
  namespace: default
  resourceVersion: "1955"
  uid: aed6557a-5462-4d6d-8e41-39216539f2f4
spec:
  replicas: 5
  selector:
    matchLabels:
      name: busybox-pod
  template:
    metadata:
      creationTimestamp: null
      labels:
        name: busybox-pod
    spec:
      containers:
      - command:
        - sh
        - -c
        - echo Hello Kubernetes! && sleep 3600
        image: busybox
        imagePullPolicy: Always
        name: busybox-container
        resources: {}
        terminationMessagePath: /dev/termination-log
        terminationMessagePolicy: File
      dnsPolicy: ClusterFirst
      restartPolicy: Always
      schedulerName: default-scheduler
      securityContext: {}
      terminationGracePeriodSeconds: 30
status:
  availableReplicas: 5
  fullyLabeledReplicas: 5
  observedGeneration: 7
  readyReplicas: 5
  replicas: 5
```

Now scale the ReplicaSet down to 2 PODs.

Use the `kubectl scale` command or edit the replicaset using `kubectl edit replicaset`.

```bash
kubectl scale --replicas=2 rs/new-replica-set
```

# 003 - Deployments

Create a new Deployment using the `deployment-definition-1.yaml` file located at `/root/`.

There is an issue with the file, so try to fix it.

```yaml
---
apiVersion: apps/v1
kind: deployment
metadata:
  name: deployment-1
spec:
  replicas: 2
  selector:
    matchLabels:
      name: busybox-pod
  template:
    metadata:
      labels:
        name: busybox-pod
    spec:
      containers:
      - name: busybox-container
        image: busybox888
        command:
        - sh
        - "-c"
        - echo Hello Kubernetes! && sleep 3600
```

<details id="bkmrk-deployment-definitio"><summary>deployment-definition-1.yaml \[Fixed\]</summary>

```yaml
---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: deployment-1
spec:
  replicas: 2
  selector:
    matchLabels:
      name: busybox-pod
  template:
    metadata:
      labels:
        name: busybox-pod
    spec:
      containers:
      - name: busybox-container
        image: busybox
        command:
        - sh
        - "-c"
        - echo Hello Kubernetes! && sleep 3600
```

</details>Create a new Deployment with the below attributes using your own deployment definition file.

Name: `httpd-frontend`;  
Replicas: `3`;  
Image: `httpd:2.4-alpine`

# 004 - Namespaces

How many pods exist in the `research` namespace?

<details id="bkmrk-solution-kubectl-get"><summary>Solution</summary>

```bash
kubectl get pods -n research
```

</details>Create a POD in the `finance` namespace.

Use the spec given below.

<div class="flex flex-col" id="bkmrk-"></div><div class="text-tx-secondary-light dark:text-tx-secondary-dark my-6" data-testid="test-result" id="bkmrk-name%3A-redis-image-na"><div class="mb-2 flex items-start justify-start space-x-[10px]"><section class="break-words w-full">- Name: redis
- Image name: redis

<details><summary>Solution</summary>

```bash
kubectl run redis --image=redis -n finance
```

</details>Which namespace has the `blue` pod in it?

<details><summary>Hint</summary>

```bash
kubectl get pods --all-namespaces 
```

</details></section></div></div>

# 005 - Imperative Commands

# Skels

# 001 - Pods

```yaml
apiVersion: v1  # Obligatorio: Versión de la API de Kubernetes.
kind: Pod       # Obligatorio: Tipo de recurso (en este caso, Pod).
metadata:
  name: <nombre-del-pod>  # Obligatorio: Nombre único del Pod.
  labels:                 # Opcional: Etiquetas para identificar el Pod.
    app: <etiqueta-app>
spec:                     # Obligatorio: Especificación del Pod.
  containers:             # Obligatorio: Lista de contenedores en el Pod.
  - name: <nombre-del-contenedor>  # Obligatorio: Nombre del contenedor.
    image: <imagen-del-contenedor>  # Obligatorio: Imagen del contenedor.
    ports:                          # Opcional: Puertos que expone el contenedor.
    - containerPort: <puerto-del-contenedor>
    env:                            # Opcional: Variables de entorno.
    - name: <nombre-de-la-variable>
      value: "<valor-de-la-variable>"
    resources:                      # Opcional: Límites y solicitudes de recursos.
      requests:
        memory: "<memoria-mínima>"
        cpu: "<cpu-mínima>"
      limits:
        memory: "<memoria-máxima>"
        cpu: "<cpu-máxima>"
  restartPolicy: Always  # Opcional: Política de reinicio (Always, OnFailure, Never).
```

# 002 - Replicasets

```yaml
apiVersion: apps/v1  # Obligatorio: Versión de la API de Kubernetes.
kind: ReplicaSet     # Obligatorio: Tipo de recurso (en este caso, ReplicaSet).
metadata:
  name: <nombre-del-replicaset>  # Obligatorio: Nombre único del ReplicaSet.
  labels:                        # Opcional: Etiquetas para identificar el ReplicaSet.
    app: <etiqueta-app>
spec:                            # Obligatorio: Especificación del ReplicaSet.
  replicas: <número-de-réplicas>  # Obligatorio: Número de Pods que deseas ejecutar.
  selector:                       # Obligatorio: Selector para identificar los Pods gestionados.
    matchLabels:
      app: <etiqueta-app>          # Debe coincidir con las etiquetas del Pod.
  template:                       # Obligatorio: Plantilla para crear los Pods.
    metadata:
      labels:                     # Obligatorio: Etiquetas del Pod.
        app: <etiqueta-app>
    spec:                         # Obligatorio: Especificación del Pod.
      containers:                 # Obligatorio: Lista de contenedores en el Pod.
      - name: <nombre-del-contenedor>  # Obligatorio: Nombre del contenedor.
        image: <imagen-del-contenedor>  # Obligatorio: Imagen del contenedor.
        ports:                          # Opcional: Puertos que expone el contenedor.
        - containerPort: <puerto-del-contenedor>
        env:                            # Opcional: Variables de entorno.
        - name: <nombre-de-la-variable>
          value: "<valor-de-la-variable>"
        resources:                      # Opcional: Límites y solicitudes de recursos.
          requests:
            memory: "<memoria-mínima>"
            cpu: "<cpu-mínima>"
          limits:
            memory: "<memoria-máxima>"
            cpu: "<cpu-máxima>"
```

# 003 - Deployments

```yaml
apiVersion: apps/v1  # Obligatorio: Versión de la API de Kubernetes.
kind: Deployment     # Obligatorio: Tipo de recurso (en este caso, Deployment).
metadata:
  name: <nombre-del-deployment>  # Obligatorio: Nombre único del Deployment.
  labels:                        # Opcional: Etiquetas para identificar el Deployment.
    app: <etiqueta-app>
spec:                            # Obligatorio: Especificación del Deployment.
  replicas: <número-de-réplicas>  # Opcional: Número de Pods que deseas ejecutar (por defecto es 1).
  selector:                       # Obligatorio: Selector para identificar los Pods gestionados.
    matchLabels:
      app: <etiqueta-app>          # Debe coincidir con las etiquetas del Pod.
  template:                       # Obligatorio: Plantilla para crear los Pods.
    metadata:
      labels:                     # Obligatorio: Etiquetas del Pod.
        app: <etiqueta-app>
    spec:                         # Obligatorio: Especificación del Pod.
      containers:                 # Obligatorio: Lista de contenedores en el Pod.
      - name: <nombre-del-contenedor>  # Obligatorio: Nombre del contenedor.
        image: <imagen-del-contenedor>  # Obligatorio: Imagen del contenedor.
        ports:                          # Opcional: Puertos que expone el contenedor.
        - containerPort: <puerto-del-contenedor>
        env:                            # Opcional: Variables de entorno.
        - name: <nombre-de-la-variable>
          value: "<valor-de-la-variable>"
        resources:                      # Opcional: Límites y solicitudes de recursos.
          requests:
            memory: "<memoria-mínima>"
            cpu: "<cpu-mínima>"
          limits:
            memory: "<memoria-máxima>"
            cpu: "<cpu-máxima>"
```