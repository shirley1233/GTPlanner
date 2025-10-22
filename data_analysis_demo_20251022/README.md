## data analysis report demo 
GTPlanner的案例中有一个模块是数据报告生成器，采用问答形式确定需求方意图生成代码和分析，故提交一份数据分析的demo，包括了简单的数据采集和使用prompt生成数据报告。


## 数据分析示例（2025-10-22）

本目录提供一个基于 CSV 的轻量级数据分析示例，包含原始数据、Jupyter Notebook 分析流程，以及导出的 HTML 报告，便于快速上手与复现。

### 文件结构
- **demo_data.csv**: 示例数据集（UTF-8 编码）。
- **csv_demo.ipynb**: 数据分析 Notebook，覆盖数据加载、清洗、探索性分析与可视化。
- **demo_data_report.html**: 由 Notebook 导出的只读报告（无需运行环境即可在浏览器查看）。

### 环境依赖
- Python 3.10.17
- 建议工具：
  - Jupyter 或 VS Code + Jupyter 插件
  - 推荐依赖（按需安装）：pandas、numpy、matplotlib、seaborn、plotly（若 Notebook 使用到交互图表）

可通过以下命令快速安装常用依赖：

```bash
pip install pandas numpy matplotlib seaborn plotly jupyter
```

### 快速开始
1. 打开报告（无需环境）：
   - 直接双击 `demo_data_report.html`，或在浏览器中打开查看分析结果。
2. 交互式复现分析流程：
   - 进入本目录后启动 Jupyter：
     ```bash
     jupyter notebook
     ```
   - 打开 `csv_demo.ipynb`，依次执行所有单元格以复现分析与图表。

### 运行 Notebook 的常见问题
- 报错缺少库：按“环境依赖”章节安装相应库后重试。
- 中文显示/乱码：
  - 确认 `demo_data.csv` 为 UTF-8 编码；
  - Matplotlib 中文字体可在 Notebook 中设置 `rcParams` 或安装中文字体。
- 图表未显示：确保在 Notebook 顶部启用了相应绘图后端（如 `%matplotlib inline`）。

### 自定义与扩展
- 替换数据：将 `demo_data.csv` 替换为同结构文件或在 Notebook 中调整读取逻辑（如列名、分隔符）。
- 导出报告：在 Jupyter 中将 Notebook 另存为 HTML（File → Download as → HTML）以生成新的只读报告。

### 复现性说明
- 本示例尽量使用固定随机种子与确定性绘图流程；如新增随机过程（抽样/模型训练），建议设置 `random_state` 以保证可复现。

### 许可证
除非上层仓库另有声明，本示例内容遵循同仓库许可协议。


