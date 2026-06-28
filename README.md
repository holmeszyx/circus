# circus
a place to store various CI actions flow

## run-flow

a composite action (`.github/actions/run-flow`) that checks out a source
repository, runs its build script, and publishes artifacts to a release in that
repository. triggered manually per target via a workflow in
`.github/workflows/`.

### usage

1. copy `.github/workflows/build-example.yml` per target, set `build-script`,
   `artifact-glob`, `runs-on`, and `branch` (default `master`), and point
   `repo-url` at the target's secret.
2. run from the Actions tab (enter the release tag).
