# rigtrans: current status and clearance

Review date: 2026-10-18 UTC. Public-safe proposed documentation. No publication or deployment authorized.

## Evidence baseline

- Public fork of vk4tmz/rigtrans.
- Master: [970be20ad99c2e0f0f0603b69858d48343dd89bd](https://github.com/cybrcwby/rigtrans/commit/970be20ad99c2e0f0f0603b69858d48343dd89bd), 2019-06-08.
- Tracked tree contains README.md and rig_trans.ps1; no issues or PRs returned during review.

## Current status

The [README](https://github.com/cybrcwby/rigtrans/blob/970be20ad99c2e0f0f0603b69858d48343dd89bd/README.md) describes a legacy TS-2000-to-FT-991/A CAT translator for Winlink use, including TX/RX handling, split-mode changes and initialization commands. Repository presence establishes neither current deployment nor compatibility.

No functional execution, connected-radio inspection or comprehensive code/security audit was performed. No actual contradiction or active deployment failure was established.

## Gates if reuse is selected

- RIGTRANS-01: decide reference-only retention versus maintained implementation. Existing purpose should be understood before rewriting it.
- RIGTRANS-02: record supported PowerShell/runtime, serial-port software, radio firmware and client versions.
- RIGTRANS-03: verify translations, malformed/unsupported commands, serial-port failures, reconnects and teardown with isolated fixtures.
- RIGTRANS-04: validate initialization, frequency/mode/split and TX/RX transitions in a nontransmitting setup before separately approved live use.
- RIGTRANS-05: review the historical ExecutionPolicy UnRestricted launch example and document an appropriately scoped method rather than implying broad policy relaxation is required.

## Closure and minimal update

A reference-only disposition closes the planning question without asserting operational readiness. Reuse clearance requires reproducible tests and recorded compatibility; a running process is not safe-radio-behavior proof.

Add a short public-safe reference-status note and relative link to this document in README. Preserve upstream attribution. Do not publish private infrastructure details or private station-document links.
