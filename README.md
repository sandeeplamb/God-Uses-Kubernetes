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

These are the values inside the Pod containers which normally remains constant and hardly changes onces the container starts.

We can define them in Deployment manifests.

There is strong point to use them by GOD for human variables which God defines only once i.e. like date-of-birth, father_name, mother_name etc.

## Human-Secrets

Kubernetes use secrets to store some secret info.

Secrets can be mount inside a container using environment variables or volumes.

If you mount secrets as volumes, eventual change in secret will happen if after deployment you want to change the values of secrets. There is no need to delete the whole deployment. In case of God, humans These can be changed on the fly.

God have more reasons to use them while deplpoying humans.

## Human-ConfigMaps

ConfigMaps unless environment variables are the values that one might want to change as per the needs during lifecycle of deployment.

God might be using them and mount it using Volumes in a human Deployment.

## Human-Deployment

This is the coolest part.

In Kubernetes, deployment creates a replica-set which watches the current state of deployment to the desired state. And if current state changes, deployment will bring with the help of replica-set to desired state. The desired state is defined in deployment manifest.

Say in case of humans, God set desired state to have 3 containers in a POD each for mother,father and sibling. But later on, their parents have one more kid, the desired state changes to 4 containers or if one of parents dies, desired state changes to 2. In this case,replica set will take care of things to bring back right amount of containers up and running.

All this can be done in Kubernetes using deployment rollback, pause, scale up, scale down with minimum of godly-like-efforts.

Just Deploy and Forget.

## Human-Service

Fine, God can create the human-deployment but how to access them when they are 7 billion
