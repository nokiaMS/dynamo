<!-- # SPDX-FileCopyrightText: Copyright (c) 2024-2026 NVIDIA CORPORATION & AFFILIATES. All rights reserved.
# SPDX-License-Identifier: Apache-2.0 -->

# SGLang

See [docs/backends/sglang/](../../../../docs/fern/backends/sglang/README.md) for documentation.

For Kimi K3.1 runtime builds, the backend imports `ConfigArgumentMerger` from
`sglang.srt.utils.server_args_config_parser`, as provided by the K3.1 engine image.
Install the Dingo wheels without the `sglang` extra to retain that image's engine
and CUDA package versions. When its Pydantic version exceeds the runtime wheel's
declared bound, use a separate Dingo virtual environment and expose the engine
site-packages with `site.addsitedir` so editable SGLang installs remain discoverable.
