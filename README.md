A simple repo that uses Github Actions + NX devtools to lint, test, build, and deploy apps automatically.

`.github/workflows/pull-request.yml` will lint, test, and build any new PRs. If any of these targets fail, the PR cannot be merged.

`.github/workflows/deploy-affected-apps.yml` will take a PR that has passed our prior checks, run a custom NX script to see which apps were affected by the PR, and then simulate a deployment via a script.

See - https://nx.dev/l/a/workspace/run-commands-executor#nx-affected
