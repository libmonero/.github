# Security Policy

This policy applies to every libmonero repository that does not have a `SECURITY.md` of its own.

## Supported versions

Security fixes are made on `main` and included in a subsequent release. Older releases are not guaranteed to receive security fixes; use the latest release where possible.

## Reporting a vulnerability

Please report vulnerabilities privately through GitHub's private vulnerability reporting: open the **Security** tab of the affected repository and choose **Report a vulnerability**. Do not disclose vulnerability details in public issues, pull requests or discussions.

If private reporting is unavailable, contact a repository maintainer privately before sharing technical details. Include the affected repository and version, the impact, and the steps to reproduce, and remove secrets or personal data from any attached logs.

These libraries handle wallets, seeds and private keys. Never post a seed, a private key or a wallet file in a report, not even one from a test wallet you still use.

## Vulnerabilities in Monero itself

The libraries build on [monero-project/monero](https://github.com/monero-project/monero). A vulnerability in Monero itself, such as in the daemon, `wallet2` or the protocol, should be reported to the Monero Project through its [Vulnerability Response Process](https://github.com/monero-project/meta/blob/master/VULNERABILITY_RESPONSE_PROCESS.md), not to libmonero.
