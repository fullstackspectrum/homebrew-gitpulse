# homebrew-gitpulse

The Homebrew tap for [GitPulse](https://github.com/fullstackspectrum/gitpulse), a CLI for GitHub traffic, clones, referrers, and release downloads that also builds org-wide HTML dashboards.

## Install

```bash
brew install fullstackspectrum/gitpulse/gitpulse
```

Or tap first, then install by name. Homebrew only loads formulae from a tap you have trusted, so trust it before installing:

```bash
brew tap fullstackspectrum/gitpulse
brew trust fullstackspectrum/gitpulse
brew install gitpulse
```

This works on macOS and Linux.

## Upgrade

```bash
brew update
brew upgrade gitpulse
```

## Uninstall

```bash
brew uninstall gitpulse
brew untap fullstackspectrum/gitpulse
```

## Usage

```bash
export GITHUB_TOKEN="$(gh auth token)"   # or a personal access token
gitpulse org ORG --open
```

See the [GitPulse README](https://github.com/fullstackspectrum/gitpulse#readme) for every command and the token permissions each one needs.

## About this tap

The formula builds GitPulse from its release on [PyPI](https://pypi.org/project/gitpulse-analytics/), where the package is named `gitpulse-analytics`. Only stable releases are published here; pre-releases are available through `pipx install --pip-args=--pre gitpulse-analytics`.

`Formula/gitpulse.rb` is updated automatically when a new version is released, so changes made to it directly in this repository will be overwritten. Report problems with the formula or with GitPulse itself on the [GitPulse issue tracker](https://github.com/fullstackspectrum/gitpulse/issues).
