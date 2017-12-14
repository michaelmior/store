# OpenFaaS Function Store

The Function Store is a curated index of OpenFaaS functions which have been tested by the community and chosen for their experience.

See the [announcement here](https://twitter.com/alexellisuk/status/936160369516654592)

![](https://pbs.twimg.com/media/DP3od15X4AEXoDI.jpg)

## Q&A

* How much does this cost?

It's free

* What's happening conceptually?

The concept is that we will keep a curated list of interesting functions that you can deploy in one-click to your existing OpenFaaS API Gateway using the UI. We do not need access to your API gateway.

We may update the CLI to make use of the store future too.

* Where are functions hosted?

In any public Docker registry whether that be the Docker Hub, Quay or elsewhere.

* Where is the list/definition kept?

We are using a .json file in this repository and GitHub's raw download CDN.

* Why is it called a store if I don't have to pay money?

See also: Google Play Store/Apple App Store.

## Make a submission

If you'd like to make a submission then raise an issue to propose it. This should follow the [CONTRIBUTION guide](https://github.com/openfaas/faas/blob/master/CONTRIBUTING.md) for OpenFaaS.

Here's an example of a function definition for the registry:

```
  {
    "title": "Inception",
    "description": "This is a forked version of the work by Magnus Erik Hvass Pedersen - it has been re-packaged as an OpenFaaS serverless function.",
    "image": "alexellis/inception",
    "name": "inception",
    "fprocess": "python3 index.py",
    "network": "func_functions",
    "repo_url": "https://github.com/faas-and-furious/inception-function",
    "labels": {
      "com.openfaas.ui.ext": "json"
    },
    "environment": {
      "write_timeout": "30"
    }
  }
```

### See also:

* `labels`

You can set the file extension used by the UI to download a result from your function i.e. csv/mp3/txt

* `environment`

Set timeouts etc
