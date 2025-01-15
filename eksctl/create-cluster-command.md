##### EKSCTL create cluster command

```
eksctl create cluster \
—name cluster \
—version 1.27 \
—region eu-central-1 \
—nodegroup-name nodes \
—node-type t2.micro \
—nodes 2 \
—nodes-min 1 \
—nodes-max 3
```
