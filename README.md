# God must be using Kubernetes !!

Gods must be using Kubernetes.

God must be Certified-Kubernetes-Admin.

I believe in the concept of re-incarnation.

Reincarnation is the philosophical or religious concept that an aspect of a living being starts a new life in a different physical body or form after each biological death.
 
And in a normal life, you follow some sequence

1. You born,
2. You do some tasks in a life (your Karma's)
3. You marry
4. You have kids
5. You get old 
6. You die 
7. Then re-born and repeat from 1-6 unless you met Supreme Conciousness

I always puzzeled that how busy God might be in order to take care of all these tasks as everyday people dies and re-born.

Not long ago, I learned new technology i.e. Kubernetes an open source Orchestrator for your microservices/containers which was Google project 
Borg before it became what it is today. 

If you are interested in growth of Kubernetes, here are some facts.

https://www.cncf.io/blog/2018/08/29/cncf-survey-use-of-cloud-native-technologies-in-production-has-grown-over-200-percent/

So just wear a God Hat and lets create a human-as-a-deployment.

```
---
apiVersion: milkyway/earthv2
kind: Reincarnation
metadata:
  name: human-deployment
  labels:
    species: homosapiens
spec:
  replicas: 1
  selector:
    matchLabels:
      species: homosapiens
  template:
    metadata:
      labels:
        species: homosapiens
    spec:
      containers:
      - name: human
        image: human:1.7.9
        env:
        - name: DATE_OF
          value: "mother"
        - name: FATHER_NAME
          value: "father"
        - name: FAMILY_LAST_NAME
          value: "LAST_NAME"
        - name: COUNTRY_BORN
          value: "India"
        args:
        - /bin/sh
        - -c
        - touch /tmp/healthy; sleep 6days; rm -rf /tmp/healthy; sleep 6days
        livenessProbe:
          exec:
            command:
            - cat
            - /tmp/healthy
          initialDelaySeconds: 5
          periodSeconds: 5
        readinessProbe:
          exec:
            command:
            - cat
            - /tmp/healthy
         initialDelaySeconds: 5
         periodSeconds: 5
        ports:
        - containerPort: 80
      initContainers:
      - name: init-myservice
        image: busybox
        command: ['sh', '-c', 'until nslookup myservice; do echo waiting for myservice; sleep 2; done;']
```

```
---
kind: MilkywayService
apiVersion: v21
metadata:
  name: accessHuman
spec:
  galaxyPort:
  - planetProtocol: Earth
    lifePort: 100
    targetYearsAlivePort: 87
```