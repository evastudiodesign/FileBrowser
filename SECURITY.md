# Security Policy

This repository is a security-maintained fork of [filebrowser/filebrowser](https://github.com/filebrowser/filebrowser), which was archived on 2026-09-01 and no longer receives fixes.

## Supported Versions

Only the `master` branch and the latest image published from it (`ghcr.io/evastudiodesign/filebrowser`) receive security fixes.

## How the fork is kept up to date

- **Dependabot** opens weekly PRs for Go modules, frontend (pnpm) packages, the Docker base images and GitHub Actions. Dependabot security updates open PRs as soon as an advisory is published.
- **Security workflow** (`.github/workflows/security.yaml`) runs `govulncheck` and `pnpm audit` on every PR, on every push to `master` and daily.
- **Image workflow** (`.github/workflows/image.yaml`) builds the container image, scans it with Grype (fails on fixable high/critical findings), and publishes it to GHCR. It also rebuilds weekly to pick up base image fixes.

## Known issues inherited from upstream

The upstream project lists known, intentionally unaddressed issue classes under [Security](README.md#security) in the README. They still apply to this fork unless a fix is noted in the changelog.

## Reporting a Vulnerability

Report privately via the [Security](https://github.com/evastudiodesign/FileBrowser/security) page of this repository. Please include, where possible:

- The commit the issue was found at
- A plaintext proof of concept (no binaries)
- Steps to reproduce
- Recommended remediation, if any
