# pytorch-mps-ci

Downstream CI repository for testing PyTorch MPS (Apple Silicon) against upstream changes, integrated through PyTorch's [Cross-Repository CI Relay](https://github.com/pytorch/pytorch/blob/main/docs/source/accelerator/ci.md).

The CRCR allowlist has this repository on nightly events only, which the relay does not dispatch. The workflow runs daily at 09:00 UTC, after the `pytorch/pytorch` `nightly` branch moves: it checks out that branch, runs MPS tests on a macOS arm64 runner, and reports the result to the relay as a nightly result for that commit.
