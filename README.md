# kustomize-bases
Stores kustomize bases of all the popular 3rd party tools used in app deployments

# WIP

## How to Use

You need to fetch the git repo of the particular base you're interested in by creating a `kustomization.yaml` in your local directory and specify the path to the repo in [hashicorp/go-getter](https://github.com/hashicorp/go-getter) URL [format](https://github.com/kubernetes-sigs/kustomize/blob/master/examples/remoteBuild.md#url-format).

For example, to get the `redis` base:

```yaml
apiVersion: kustomize.config.k8s.io/v1beta1
kind: Kustomization
namespace: my-app-namespace
resources:
- https://github.com/mr-karan/kustomize-bases/redis
```
