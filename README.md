# Scyther for Windows 11 (Modified Version)

本项目是对原始 [Scyther 安全协议验证工具](http://www.cs.ox.ac.uk/people/cas.cremers/scyther/index.html) 的改进版本，已完成以下兼容性适配与增强：

- ✅ 支持 **Windows 11** 系统完整运行；
- ✅ 提供可用的 `scyther-gui.py` 图形用户界面（基于 `wxPython`）；
- ✅ 使用 `conda` 环境统一管理依赖，便于部署；
- ✅ 内置协议模型测试文件（`.spdl`），可用于验证与学习。

原始项目由 Cas Cremers 维护，源代码托管于：
👉 https://github.com/cascremers/scyther

---

## 📦 安装与环境配置

### 1. 克隆项目

```bash
git clone https://github.com/TMXJ520/Scyther-win64.git
cd Scyther-win64
```
### 2. 创建 Conda 虚拟环境（推荐）
确保已安装 Anaconda 或 Miniconda，然后执行：
```bash
conda env create -f environment.yml
conda activate scyther
```
这将自动安装包括 wxPython、Python 3.x 在内的全部运行依赖。

## 🚀 使用说明
### 方式一：图形界面运行（GUI）
```bash
python ./scyther-gui.py
```
若界面无法启动，请确认当前在 scyther Conda 环境中，且 wxPython 安装成功。

### 方式二：命令行运行（CLI）
在根目录下使用预编译的可执行文件：

```bash
./scyther-w32.exe -i .\Protocols\example.spdl
```
scyther-w32.exe 是适用于 Windows 的二进制主程序。

## 📁 项目结构说明
| 路径/文件                | 说明                          |
| -------------------- | --------------------------- |
| `scyther-gui.py`     | 图形用户界面启动脚本                  |
| `scyther-w32.exe`    | Windows 下的 Scyther 命令行可执行文件 |
| `environment.yml`    | Conda 虚拟环境配置文件              |
| `Protocols/`         | 示例协议模型（`.spdl` 格式）文件目录      |
| `scyther-manual.pdf` | 当前版本的 Scyther 使用手册（可能不完整）   |
| `tests/`             | 原始项目附带的脚本测试目录（主要用于 Linux）   |


## 🔬 协议建模与验证说明
Scyther 使用 .spdl 格式的脚本进行安全协议建模，并支持如下功能：

- 多角色建模
- 身份验证与密钥协商过程建模
- 安全属性声明（如 secrecy、authentication）
- 图形化查看消息流程
- 自动符号验证与攻击路径发现

如需创建自己的协议模型，请参考 Protocols/ 目录下的示例文件。

## 📝 开发与适配说明
该项目在以下环境下开发并测试通过：

- 操作系统：Windows 11 64 位
- Conda 版本：conda 23.x
- Python 版本：3.9（由 environment.yml 指定）
- GUI 框架：wxPython >= 4.1.1

## 📜 许可证（License）
本项目基于原始 Scyther 工具，遵循 GNU General Public License v2.0 (GPL-2.0)。
原始版权归 Cas Cremers 所有。修改版本仅用于研究与学习用途，如有商用需求请联系原作者。

## 🙋 联系与致谢
本项目由 TMXJ520 修改与维护，用于安全协议学习、教学演示与形式化验证实验。
欢迎提交 Issue 反馈运行问题，或提出改进建议。








