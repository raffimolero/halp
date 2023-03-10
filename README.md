<div align="center">

  <a href="https://lospec.com/gallery/orhun/octopus">
    <img src="assets/halp-logo.png" width="400">
  </a>

<h4>A CLI tool to get help with CLI tools 🐙</h4>

<!--
TODO: Uncomment these
<a href="https://github.com/orhun/halp/releases"><img src="https://img.shields.io/github/v/release/orhun/halp?style=flat&amp;labelColor=342a5e&amp;color=684d81&amp;logo=GitHub&amp;logoColor=white" alt="GitHub Release"></a>
<a href="https://crates.io/crates/halp/"><img src="https://img.shields.io/crates/v/halp?style=flat&amp;labelColor=342a5e&amp;color=684d81&amp;logo=Rust&amp;logoColor=white" alt="Crate Release"></a>
<a href="https://codecov.io/gh/orhun/halp"><img src="https://img.shields.io/codecov/c/gh/orhun/halp?style=flat&amp;labelColor=342a5e&amp;color=684d81&amp;logo=Codecov&amp;logoColor=white" alt="Coverage"></a>
<br>
<a href="https://github.com/orhun/halp/actions?query=workflow%3A%22Continuous+Integration%22"><img src="https://img.shields.io/github/actions/workflow/status/orhun/halp/ci.yml?branch=main&amp;style=flat&amp;labelColor=1c1d42&amp;color=4f396a&amp;logo=GitHub%20Actions&amp;logoColor=white" alt="Continuous Integration"></a>
<a href="https://github.com/orhun/halp/actions?query=workflow%3A%22Continuous+Deployment%22"><img src="https://img.shields.io/github/actions/workflow/status/orhun/halp/cd.yml?style=flat&amp;labelColor=1c1d42&amp;color=4f396a&amp;logo=GitHub%20Actions&amp;logoColor=white&amp;label=deploy" alt="Continuous Deployment"></a>
<a href="https://hub.docker.com/r/orhunp/halp"><img src="https://img.shields.io/github/actions/workflow/status/orhun/halp/docker.yml?style=flat&amp;labelColor=1c1d42&amp;color=4f396a&amp;label=docker&amp;logo=Docker&amp;logoColor=white" alt="Docker Builds"></a>
<a href="https://docs.rs/halp/"><img src="https://img.shields.io/docsrs/halp?style=flat&amp;labelColor=1c1d42&amp;color=4f396a&amp;logo=Rust&amp;logoColor=white" alt="Documentation"></a>
-->

</div>

<!-- TODO: Add GIF -->

Have you ever experienced this:

```sh
$ some_tool -v
unknown flag -v

$ some_tool -V
unknown flag -V

$ some_tool -h
unknown flag -h

$ asdjw1jwhdajh1idojad # frustration
bash: asdjw1jwhdajh1idojad: command not found

$ some_tool --help
Some CLI Tool Version 1.42.69
Usage:
  some_tool <flags> <args> [--parameter1 value1 --parameter2 value2 ...]

# f*cking finally!
```

`halp` aims to help with this and other different cases.

## Installation

<details>
  <summary>Packaging status</summary>

[![Packaging status](https://repology.org/badge/vertical-allrepos/halp.svg)](https://repology.org/project/halp/versions)

</details>

### Cargo

`halp` can be installed from [crates.io](https://crates.io/crates/halp):

```sh
cargo install halp
```

The minimum supported Rust version is `1.64.0`.

### Arch Linux

`halp` can be installed from available [AUR packages](https://aur.archlinux.org/packages/?O=0&SeB=b&K=halp&outdated=&SB=n&SO=a&PP=50&do_Search=Go) using an [AUR helper](https://wiki.archlinux.org/index.php/AUR_helpers). For example,

```sh
paru -S halp
```

If you prefer, you can clone the package and then build it with [makepkg](https://wiki.archlinux.org/index.php/Makepkg). For example,

```sh
git clone https://aur.archlinux.org/halp.git && cd halp && makepkg -si
```

### Docker

#### Images

Docker builds are [automated](./.github/workflows/docker.yml) and images are available in the following registries:

- [Docker Hub](https://hub.docker.com/r/orhunp/halp)
- [GitHub Container Registry](https://github.com/orhun/halp/pkgs/container/halp)

#### Usage

The following commands can be used to get help for a binary inside the container:

```sh
docker run --rm -it "orhunp/halp:${TAG:-latest}" whoami
docker run --rm -it "orhunp/halp:${TAG:-latest}" plz whoami
```

Or you can provide a custom binary as follows (please note that you might get shared library errors):

```sh
docker run -v "bin:/app/bin:rw" --rm -it "orhunp/halp:${TAG:-latest}" -v ./bin
```

#### Building

Custom Docker images can be built from the [Dockerfile](./Dockerfile):

```sh
docker build -t halp .
```

### Binary releases

See the available binaries for different targets from the [releases page](https://github.com/orhun/halp/releases). They are are automated via [Continuous Deployment](.github/workflows/cd.yml) workflow

Release tarballs are signed with the following PGP key: [0xFB41AE0358378256](https://keyserver.ubuntu.com/pks/lookup?search=0xFB41AE0358378256&op=vindex)

### Build from source

1. Clone the repository.

```sh
git clone https://github.com/orhun/halp && cd halp/
```

2. Build.

```sh
CARGO_TARGET_DIR=target cargo build --release
```

Binary will be located at `target/release/halp`.

## Usage

## Configuration

## License

<sup>
Licensed under either of <a href="LICENSE-APACHE">Apache License, Version
2.0</a> or <a href="LICENSE-MIT">MIT license</a> at your option.
</sup>

<br>

<sub>
Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in this program by you, as defined in the Apache-2.0 license,
shall be dual licensed as above, without any additional terms or conditions.
</sub>
