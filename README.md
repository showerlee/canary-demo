# Canary demo

> Version B is released to a subset of users, then proceed to a full rollout.

![kubernetes canary deployment](./docs/grafana-canary.png)

A canary deployment consists of gradually shifting production traffic from
version A to version B. Usually the traffic is split based on weight. For
example, 90 percent of the requests go to version A, 10 percent go to version B.

This technique is mostly used when the tests are lacking or not reliable or if
there is little confidence about the stability of the new release on the
platform.

You can apply the following canary deployment techniques:

- [Native](native/) way by adjusting the number of replicas.

- [Istio](istio/) way by adjusting the weight in VirtualService.

- [Nginx-ingress](nginx-ingress/) way by defining fine grained traffic splitting via Ingress annotations.

