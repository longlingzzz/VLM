# 第三方研究代码

## From Head to Tail / VLMLT

- 拉取日期：2026-10-10。
- 作者仓库：[ssmisya/VLMLT](https://github.com/ssmisya/VLMLT)。
- 本地目录：`third_party/VLMLT/`，以 Git 子模块纳入父项目，保留作者原始提交历史。
- 分支：`main`。
- 拉取时提交：`f2d327fdf7fb1ec99a997703ff6c8245e36d2505`（2025-06-06，`fix readme`）。
- 登记时子模块工作区无修改；父项目通过 `.gitmodules` 和固定提交引用跟踪源码，并保留本记录。

【本次已核实】已在本地确认 `reverse_indexing.py`、`reform_data_one_scope.py` 和 `diffusion_inference.py` 存在。训练目录包含 LLaMA-Factory、LLaVA、LLaVA-NeXT、ShareGPT4V 四个 Git 子仓库引用，但作者主仓库没有 `.gitmodules`，本次没有展开这些目录。

本次仅拉取源码，没有安装依赖、执行作者脚本、另行下载数据／权重或启动训练。此前方法与工程核查见 [PMLL 引用论文源码核查](../docs/PMLL引用论文源码核查-2026-10-08.md)。后续修改与实验需记录相应代码版本和本地变更。

在其他电脑克隆本项目后，于项目根目录拉取已登记的作者版本：

```bash
git submodule update --init -- third_party/VLMLT
```

该命令只初始化本项目登记的 VLMLT；作者仓库内上述四个缺配置的训练框架引用仍需另行整理。
