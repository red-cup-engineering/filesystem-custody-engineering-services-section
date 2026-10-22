# Filesystem Custody Services Section

<!-- 561-group-standards:badges:start -->
[![Red Cup Engineering](https://img.shields.io/badge/561%20Group-Red%20Cup%20Engineering-c0392b)](https://github.com/red-cup-engineering)
[![License: MIT](https://img.shields.io/badge/license-MIT-c0392b)](LICENSE)
[![Indigenous data: CARE](https://img.shields.io/badge/Indigenous%20data-CARE-4b6f44)](https://github.com/red-cup-engineering/.github/blob/main/GOVERNANCE.md)
[![Tips welcome](https://img.shields.io/badge/tips-welcome-d4a017)](https://github.com/561-group/.github/blob/main/TIPS.md)
<!-- 561-group-standards:badges:end -->

This is the POSIX workspace boundary. It admits bounded reads and
compare-and-swap writes, records immutable receipts in an append-only outbox,
and exposes no Git operation. A version-control service may settle an accepted
receipt later; it may never infer a change from ambient worktree dirt.

The provider is intentionally placed under file services. The retired
`block-device-io-coordinator` is preserved in the version-control legacy
catalog and is not part of this service's runtime boundary.
