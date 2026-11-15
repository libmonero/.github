# Contributing

Thank you for helping. This guide applies to every libmonero repository that does not have a `CONTRIBUTING.md` of its own. Where a repository has one, follow that one.

## Before you start

* **Bugs and questions:** open an issue in the repository concerned, with the version, the platform, and the steps to reproduce. Remove seeds, private keys, passwords and wallet files from anything you paste.
* **Large changes:** open an issue first, so two people don't write the same thing.
* **Security problems:** do not open an issue. Follow the [security policy](SECURITY.md).

## One data model, many languages

The libraries share a [data model and API specification](https://github.com/libmonero/monero-python/blob/main/docs/monero-spec.pdf), so a change to the API usually lands in more than one repository.

* Names and behavior follow the shared interfaces (`MoneroWallet`, `MoneroDaemon` and the model classes), and each language keeps its own conventions for casing and idioms.
* If you change the data model or add a call, say so in the description and link the changes in the other repositories, or say that they are still to do.
* A test that exists in one language can usually be ported to the others. [monero-python](https://github.com/libmonero/monero-python) is the reference for the tests.

## Pull requests

* One topic per pull request, started from `main`. Don't build it on another open pull request.
* Keep it small. Each commit should build and pass the tests on its own, so squash the fixups before asking for a review.
* Say in the description what changed and how you tested it. A couple of lines is enough.
* Change submodule pins, workflows and build configuration in a pull request that is about that and nothing else.
* Code taken from someone else's pull request gets a `Co-authored-by` trailer in its commit, and the description says where it came from.

## Tests

* A change comes with its tests, and a fix with a test that fails without it.
* Run the unit tests before you push. Integration tests need a node and a wallet RPC server, and each repository explains how to start them, usually with the images of [docker-monero-rpc](https://github.com/libmonero/docker-monero-rpc) on regtest.
* Never test against mainnet with funds you can't lose. Use regtest, stagenet or testnet.

## Secrets

Seeds and private keys are never logged, printed or committed, and test fixtures only contain wallets created for testing.

## License

By contributing you agree that your contribution is released under the license of the repository you contribute to.
