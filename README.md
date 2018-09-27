# God must be using Kubernetes !!

Gods must be using Kubernetes to manage humans birth cycle. God must be Certified-Kubernetes-Admin.

Lets Prove

## What is Reincarnation
Reincarnation is the philosophical or religious concept that an aspect of a living being starts a new life in a different physical body or form after each biological death.
 
And in a normal life cycle, you follow some sequence

1. You born,
2. You do some tasks in a life (your Karma's)
3. You marry
4. You have kids
5. You get old 
6. You die 
7. Then re-born and repeat from 1-6 unless you met Supreme Conciousness

I always puzzeled that how busy God might be in order to take care of all these tasks as everyday people dies and re-born.

Not long ago, I learned new technology i.e. [Kubernetes](https://kubernetes.io/) an open source Orchestrator for your microservices/containers which was Google project 
Borg before it became what it is today. 

If you are interested in growth of Kubernetes, here are some facts.

[Rise Of Kubernetes](https://www.cncf.io/blog/2018/08/29/cncf-survey-use-of-cloud-native-technologies-in-production-has-grown-over-200-percent/)

So just wear a God Hat and lets create a **human-as-a-deployment**.

# The Original LifeCycle - Life - How God might be managing?

## Human-Conciousness-Storage

As humans lives-dies-repeat in a cycle and his conciousness of all life is accessible in any life, God must be using some sort of persistance storage.

And this storage must be **retained** after every time human dies, but if we want, we can access it later or bound it to same human in other life.

Kubernetes have same concept of [Storage Class](https://kubernetes.io/docs/concepts/storage/storage-classes/), [Persistent Volume](https://kubernetes.io/docs/concepts/storage/persistent-volumes/) and [Persistent Volume Claim](https://kubernetes.io/docs/concepts/storage/persistent-volumes/#persistentvolumeclaims).

**Storage Classes** are used to do dynamically provision Persistent Volumes.

**Persistent Volumes** used to store data. There is concept of persistentVolumeReclaimPolicy which can be either Recycle, Retain or Delete.

Recycle policy, it deletes the volume’s contents and makes the volume available to be claimed again. This way,the PersistentVolume can be reused multiple times by different PersistentVolume-Claims and different pods

The Delete policy, on the other hand, deletes the underlying storage

Retain policy will retain the data even after PVC is released.

**God might be using Retain policy and in case of non-humans Recycle policy**

**Persistent Volume Claims** is a way to consume the PV created above. It may ask the Storage Class to be used or accessModes to access the data.

**Looks God is using them consistently.**

## Human-Environment-Variables

These are the values inside the Pod containers which normally remains constant and hardly changes once the pod/container starts.

We can define them in Deployment manifests.

There is strong point to use them by GOD  as some human-variables must be defined only once i.e. like date-of-birth, father_name, mother_name etc.

## Human-Secrets

Kubernetes use secrets to store secret info.

Secrets can be mounted inside a container using environment variables or volumes.

If you mount secrets as volumes, eventual change in secret will happen if after deployment you want to change the values of secrets. There is no need to delete the whole deployment. 

In case of humans, God dont need to kill a person if he wants to change the luck, job, spouses, kids etc. He just need to update the config with new details and thats it. Person have now totally different chosen path.

## Human-ConfigMaps

ConfigMaps unless environment variables are the values that one might want to change as per the needs during lifecycle of deployment.

God will be mounting ConfigMaps using Volumes in a human Deployment.

Very interesting property of ConfigMaps is the actual size of ConfigMap can not be more than 1MB.

In case of human-deployment, we have seen that there is a limit on every circumstances, abilities that we can perform.

Changing size of 1MB is not impossible but can be customised. And same with God, if he wants he can increase the capabilites of certain human. Just config management for him.

## Human-Deployment

This is the coolest part.

In Kubernetes, deployment creates a replica-set which watches the current state of deployment to the desired state. And if current state changes, deployment will bring with the help of replica-set to desired state. The desired state is defined in deployment manifest.

Say in case of humans, God set desired state to have 3 containers in a POD each for mother,father and sibling. But later on, their parents have one more kid, the desired state changes to 4 containers or if one of parents dies, desired state changes to 2. In this case,replica set will take care of things to bring back right amount of containers up and running.

All this can be done in Kubernetes using deployment rollback, pause, scale up, scale down with minimum of godly-like-efforts.

Just Deploy and Forget.

## Human-Service

Fine, God can create the human-deployment but how to access them when they are 7 billion humans and keeps on increasing.

There are 3 types of services that Kubernetes offers - ClusterIP, NodePort and LoadBalancer and the type can be changed at any point of time in the process.

You can start with ClusterIP service and then can change to NodePort and ultimately to give access to whole world, can make it a LoadBalancer type.

In case of God, he starts with ClusterIP - access only to Parents i.e. local access.

Then changes to NodePort means human takes cares of his own responsibility. Parents not needed.

And then when human dies or get Nirvana, make the service type to LoadBalancer. Human is accessible from everywhere.

## Human-DaemonSet

The concept of Parallel-Universe says there is exact replica of you in another Univerese and the environment or circumstances can be totally different.

In case of Kubernetes, Pods can run in one node or 2 nodes decided by scheduler. 

For example, if there are 5 worker nodes and you have a deployment with 1 container. When Kubernetes schedules the deployment pod, this pod will be scheduled to only 1 node. But there can be circumstances where you want to run this pod in every possible nodes of a cluster.

Here comes the DaemonSet Deployment. You create a daeomonset and Kubernetes will make sure every node have your pod running. And every node have different resources available at given time than the other nodes in cluster.

Same like you have exact replica of yourself in every Universe but may not be in same circumstances.

## Custom-Resource-Definitions CRD's

So if you have special usecase and Kubernetes native resources are not enough for you to use, Kubernetes loose coupling helps users to create own scheduler, custom-resources to make solution Kubernetes native as per the needs.

So where God might be using CRD's. For God, if you are concious enough you can create your own way to acheive your goals. Differnet religions in world are just CRD's to make customized solution but with the help of Kubernetes or God.

