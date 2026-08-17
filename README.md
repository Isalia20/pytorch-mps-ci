# pytorch-mps-ci

Downstream CI repository for testing PyTorch MPS (Apple Silicon) against upstream changes, integrated through PyTorch's [Cross-Repository CI Relay](https://github.com/pytorch/pytorch/blob/main/docs/source/accelerator/ci.md).

The relay dispatches `repository_dispatch` events for `pytorch/pytorch` pull requests and pushes. The workflow in this repository checks out PyTorch at the dispatched commit and runs MPS tests on a macOS arm64 runner.
