---
title: vendir.lock.yml spec
---

Lock file is generated by `vendir sync` and is placed next to related `vendir.yml`.

```yaml
apiVersion: vendir.k14s.io/v1alpha1
kind: LockConfig

directories:
- path: config/_ytt_lib
  contents:
  - path: github.com/cloudfoundry/cf-k8s-networking

    # present if this is managed manually
    manual: {}

    # present if git
    git:
      # resolved checked out commit SHA
      sha: 2b009b61fa8afb330a4302c694ee61b11104c54c
      # resolved checked out commit title
      commitTitle: 'feat: add /metrics prometheus scrapable endpoint...'
      # resolved to a set of tags pointing to sha (v0.11.0+)
      tags:
      - "4.0.0"

    # present if github release
    githubRelease:
      # resolved release url
      url: https://api.github.com/repos/pivotal/kpack/releases/22747441

    # present if helm chart (v0.11.0+)
    helmChart:
      appVersion: "5.0.7"
      version: "10.5.7"

    # present if http
    http: {}

    # present if image (v0.11.0+)
    image:
      # fully resolve image URL with digest
      url: index.docker.io/dkalinin/consul-helm@sha256:d1cdbd46561a144332f0744302d45f27583fc0d75002cba473d840f46630c9f7

    # present if inline (v0.11.0+)
    inline: {}

    # present if this was sourced from local directory
    directory: {}
```
