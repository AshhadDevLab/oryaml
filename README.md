# ⚡ oryaml

**The fastest YAML parser for Python, written in Rust.**

> ⚠️ **Status: UNDER ACTIVE DEVELOPMENT** > This library is currently in **Pre-Alpha**.  
> **Do not use in production environments** until the v0.1.0 release.

## 🚀 The Goal
`oryaml` aims to be for YAML what `orjson` is for JSON: a drop-in replacement that exploits Rust's zero-cost abstractions to achieve blazing-fast parsing speeds.

## 📊 Early Benchmarks

Even in this early prototype stage, `oryaml` is significantly faster than the standard `PyYAML` library.

| Library | Parsing Time (50k records) | Speedup |
| :--- | :--- | :--- |
| **PyYAML (CLoader)** | ~117.32s | 1x |
| **ruamel.yaml** | ~156.84s | 0.7x |
| **oryaml (v0.0.1)** | **~12.00s** | **~9.7x** 🚀 |

*(Benchmarks run on a ~106MB complex YAML file with deep nesting)*

**Performance Targets:**
Internal tests show potential for further significant reductions in parsing time as the engine matures. We are targeting a sub-4-second parse time for this dataset in the v0.1.0 release.

## 📦 Installation

*Coming soon to PyPI.*

To build from source:
```bash
git clone https://github.com/AshhadDevLab/oryaml.git
cd oryaml
maturin develop --release
