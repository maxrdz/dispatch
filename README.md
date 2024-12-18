# Dispatch

A graphical application for sending SMS/MMS messages, built with libcosmic
for the COSMIC desktop environment, and in the future, the COSMIC mobile
shell.

A **justfile** is included by default with common recipes used by other
COSMIC projects.

- `just` builds the application with the default `just build-release` recipe
- `just run` builds and runs the application
- `just install` installs the project into the system
- `just vendor` creates a vendored tarball
- `just build-vendored` compiles with vendored dependencies from that tarball
- `just check` runs clippy on the project to check for linter warnings
- `just check-json` can be used by IDEs that support LSP


## Cross Compiling

PLEASE install cross-rs via:

    cargo install cross --git https://github.com/cross-rs/cross

The cross project is in a weird state where it doesn't have much motivation
and/or time to cut a release, so you need to pull from the main branch to
get a lot of bug fixes since the 'latest' release as of December 2024.

Cross compilation is weird.

We emulate arm64 within a Docker container.

Install:

    docker run --privileged --rm tonistiigi/binfmt --install arm64

