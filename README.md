[update-readmes]   Mode: rewrite — migrating to template structure...
# ratchet

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/ratchet)

<!-- AI:start:what-it-does -->
_Description pending._
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
_Architecture documentation pending._
<!-- AI:end:architecture -->

## Install

<!-- Add installation instructions here. This section is yours — the AI will not modify it. -->

```bash
git clone https://github.com/Interested-Deving-1896/ratchet.git
cd ratchet
```

## Usage


For more information about available commands and options, run a command with
`-help` to use detailed usage instructions.

#### Pin

The `pin` command pins to specific versions:

```shell
# pin the input file
ratchet pin workflow.yml

# pin a circleci file
ratchet pin -parser circleci circleci.yml

# pin a cloudbuild file
ratchet pin -parser cloudbuild cloudbuild.yml

# pin a drone file
ratchet pin -parser drone drone.yml

# pin a gitlab file
ratchet pin -parser gitlabci gitlabci.yml

# output to a tekton file
ratchet pin -out -parser tekton tekton.yml

# output to a different path
ratchet pin -out workflow-compiled.yml workflow.yml
```

#### Unpin

The `unpin` command unpins any pinned versions:

```shell
# unpin the input file
ratchet unpin workflow.yml

# output to a different path
ratchet unpin -out workflow.yml workflow-compiled.yml
```

#### Update

The `update` command updates all versions to the latest matching constraint:

```shell
# update the input file
ratchet update workflow.yml

# update a circleci file
ratchet update -parser circleci circleci.yml

# update a cloudbuild file
ratchet update -parser cloudbuild cloudbuild.yml

# output to a different path
ratchet update -out workflow-compiled.yml workflow.yml
```

#### Upgrade

> [!NOTE]
> This command only works with GitHub Actions references. It does not support
> container or Docker-based references.

The `upgrade` command upgrades all versions to the latest version, changing the
ratchet comment and also updating the ref.

```shell
# upgrade the input file
ratchet upgrade workflow.yml

# output to a different path
ratchet upgrade -out workflow-compiled.yml workflow.yml
```

> [!NOTE]
> Performs an `update` if the constraint ref is for a branch.

#### Lint

The `lint` command reports if all versions are pinned, printing any violations,
and exiting with a non-zero error code when entries are not pinned:

```shell
ratchet lint workflow.yml
```

## Configuration

<!-- Document configuration options here. This section is yours — the AI will not modify it. -->

## CI

<!-- AI:start:ci -->
The repository uses GitHub Actions for continuous integration. The following workflows are defined:

1. **`test.yml`**  
   - Runs tests and lints the codebase.  
   - Steps include setting up Go, installing dependencies, running linters, and executing tests.  
   - No secrets are required.

2. **`release.yml`**  
   - Builds and publishes a release using GoReleaser.  
   - Triggered on version tags.  
   - Requires the following secrets:
     - `GITHUB_TOKEN`: Automatically provided by GitHub for authentication.
     - `DOCKER_USERNAME`: Docker Hub username for publishing images.
     - `DOCKER_PASSWORD`: Docker Hub password for authentication.
<!-- AI:end:ci -->

## Mirror chain

<!-- AI:start:mirror-chain -->
This repo is maintained in [`Interested-Deving-1896/ratchet`](https://github.com/Interested-Deving-1896/ratchet) and mirrored through:

```
Interested-Deving-1896/ratchet  ──►  OpenOS-Project-OSP/ratchet  ──►  OpenOS-Project-Ecosystem-OOC/ratchet
```

Changes flow downstream automatically via the hourly mirror chain in
[`fork-sync-all`](https://github.com/Interested-Deving-1896/fork-sync-all).
Direct commits to OSP or OOC are detected and opened as PRs back to `Interested-Deving-1896`.
<!-- AI:end:mirror-chain -->

## Contributors

<!-- AI:start:contributors -->
_Contributors pending._
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
[Apache-2.0](https://github.com/Interested-Deving-1896/ratchet/blob/main/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
