# Grafana Platform Tests

This repository houses smoke, acceptance, and load tests for Grafana as a
platform. 

Teams building plugins, datasources, or apps, can add tests to this repo and
have them run with [Bench](https://github.com/grafana/grafana-bench) in CI.

## How does it work?

Each team adds a `bench/` directory to their repository and installs the `bench`
github action workflow. The action will:

1. look for the `bench/` directory in the repo
2. run the tests
3. if the tests pass, open a PR to `grafana-platform-tests` where they will be
   run through CI again

Once tests are merged in the `grafana-platofmr-tests` repo, they will be run in
the Grafana Rolling Release Channels
