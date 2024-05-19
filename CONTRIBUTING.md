# Contributing to CoreDNS Helm Chart

Welcome! Our community focuses on helping others and making CoreDNS the best it can be. We gladly accept contributions and encourage you to get involved!

## Issues

Before opening a new issue please search the [issue list](https://github.com/coredns/helm/issues) to ensure the issue hasn't been already reported.

If not, [open an issue](https://github.com/coredns/coredns/issues) and answer the questions so we can understand and reproduce the problematic behavior.

Please be aware that CoreDNS can be extremely flexible and offered as an add-on by many distros. While we strive to keep an open mind about supporting as many use cases as possible, we want to focus on things that fit *this* chart's use cases and not on a specific vendor installation or offering of CoreDNS.

## Pull Requests

Submit minor improvements or changes any time. For larger changes please raise an issue beforehand so we can coordinate the work and make sure the change is aligned with the chart's purpose.

When submitting a pull request, please be mindful of the following:

### Versioning

We follow the [semver standard](https://semver.org/) for versioning.

Please ensure chart version changes adhere to semantic versioning standards:

* Major: Large chart rewrites, major non-backwards compatible or destructive changes
* Minor: New chart functionality (sidecars), major application updates or minor non-backwards compatible changes
* Patch: App version patch updates, backwards compatible optional chart features

### Changelog

As the chart is also published on Artifact Hub, we require a changelog per new chart release. Changes on a chart must be documented in a chart specific changelog in the `Chart.yaml` [Annotation Section](https://helm.sh/docs/topics/charts/#the-chartyaml-file).

A new `artifacthub.io/changes` needs to be written covering only the changes since the previous release. Each change requires a new bullet point following the pattern. See more information [Artifact Hub annotations in Helm Chart.yaml file](https://artifacthub.io/docs/topics/annotations/helm/).

```yaml
- kind: {type}
  description: {description}
```

You can use the following template:

```yaml
name: coredns
version: 1.19.6
...
annotations:
  artifacthub.io/changes: |
    - kind: added
      description: Something New was added
    - kind: changed
      description: Changed Something within this chart
    - kind: changed
      description: Changed Something else within this chart
    - kind: deprecated
      description: Something deprecated
    - kind: removed
      description: Something was removed
    - kind: fixed
      description: Something was fixed
    - kind: security
      description: Some Security Patch was included
```

### Developer Certificate of Origin

As required by the CNCF's [charter](https://github.com/cncf/foundation/blob/master/charter.md#11-ip-policy),
all new code contributions must be accompanied by a [Developer Certificate of Origin (DCO)](https://developercertificate.org/). CoreDNS uses [Probot](https://github.com/probot/dco#how-it-works) to enforce the DCO on pull requests.

You may use git option `-s` to append automatically to the `Sign-off-by` line to your commit messages:

```
$ git commit -s -m 'This is my commit message'
```

# Thank You

Thanks for your help! CoreDNS would not be what it is today without your contributions.
