# PPT自动重新设计工具 🎨

一个使用Python自动分析、优化和重新设计PPT文件的工具。

## 功能特性 ✨

- 📋 **自动分析PPT内容** - 提取文本、图片和布局信息
- 🎨 **应用设计主题** - 支持现代、专业、创意三种风格
- 📐 **优化布局** - 自动调整文本和图片的位置
- 💾 **保存新PPT** - 生成重新设计后的PPT文件

## 支持的设计主题

- **modern** (现代) - 蓝色主色，适合科技公司
- **professional** (专业) - 深蓝色主色，适合正式场合
- **creative** (创意) - 紫色主色，适合创意行业

## 安装 🚀

### 1. 克隆仓库
```bash
git clone https://github.com/lucieliu/ppt-redesign.git
cd ppt-redesign
```

### 2. 安装依赖
```bash
pip install -r requirements.txt
```

## 使用方法 📖

### 基础用法

将你的PPT文件放在项目根目录，然后运行：

```bash
python ppt_redesigner.py
```

脚本会自动：
1. 查找所有PPT文件
2. 分析内容
3. 应用现代主题
4. 优化布局
5. 保存新PPT（文件名后缀为 `_redesigned.pptx`）

### 自定义使用

在Python中使用：

```python
from ppt_redesigner import PPTRedesigner

# 创建重新设计器
redesigner = PPTRedesigner('你的文件.pptx')

# 执行重新设计 (选择主题: 'modern', 'professional', 'creative')
redesigner.redesign(theme='professional', optimize=True)
```

## 输出示例

运行脚本后，你会看到：

```
🔍 找到 1 个PPT文件

处理: 地热纤知-5.29会后(1)(1).pptx
✅ 成功加载PPT文件: 地热纤知-5.29会后(1)(1).pptx
📊 总共有 5 张幻灯片

============================================================
🚀 开始PPT重新设计流程
============================================================

📋 PPT内容分析
...
🎨 应用 'modern' 主题...
✅ 主题应用完成
📐 优化布局...
✅ 布局优化完成
✅ 重新设计的PPT已保存: 地热纤知-5.29会后(1)(1)_redesigned.pptx

============================================================
✨ PPT重新设计完成！
============================================================
```

## 文件结构 📁

```
ppt-redesign/
├── README.md              # 项目说明文档
├── requirements.txt       # Python依赖
├── ppt_redesigner.py     # 核心脚本
├── .gitignore            # Git忽略配置
└── 地热纤知-5.29会后(1)(1).pptx  # 你的PPT文件
```

## 主要功能详解 🎯

### 1. 内容分析
自动扫描PPT文件，提取：
- 所有文本内容
- 图片数量和位置
- 幻灯片布局信息

### 2. 主题应用
支持三种预设主题，自动调整：
- 文本颜色
- 标题和正文样式
- 整体配色方案

### 3. 布局优化
智能调整幻灯片布局：
- 文本和图片的相对位置
- 元素大小和间距
- 页面整体平衡

## 下一步计划 🔮

未来可能添加的功能：

- [ ] 集成OpenAI API获取AI设计建议
- [ ] 支持更多自定义选项
- [ ] 批量处理多个PPT文件
- [ ] 自动生成配色方案
- [ ] 图片质量优化
- [ ] 字体自动调整
- [ ] 添加动画效果
- [ ] 导出为其他格式

## 技术栈 🛠️

- **python-pptx** - PPT文件操作库
- **Pillow** - 图片处理库
- **OpenAI** - AI辅助（将来使用）

## 故障排除 🔧

### 问题：找不到PPT文件
**解决方案：** 确保PPT文件在项目根目录或子目录中，且文件格式为 `.pptx`

### 问题：导入错误
**解决方案：** 运行以下命令确保所有依赖都已安装：
```bash
pip install -r requirements.txt
```

### 问题：权限错误
**解决方案：** 确保你有读写PPT文件的权限

## 快速开始步骤

1. **克隆或下载项目**
2. **安装依赖**: `pip install -r requirements.txt`
3. **放入你的PPT文件**
4. **运行脚本**: `python ppt_redesigner.py`
5. **查看结果**: `_redesigned.pptx` 文件

## 自定义配置

编辑 `ppt_redesigner.py` 中的主题色定义：

```python
themes = {
    'modern': {
        'primary': RGBColor(0, 120, 215),      # 修改主色
        'secondary': RGBColor(50, 50, 50),     # 修改次色
        'accent': RGBColor(255, 150, 0)        # 修改强调色
    },
    # ... 其他主题
}
```

## 许可证

MIT License

## 贡献指南

欢迎提交Issue和Pull Request！

## 联系方式

如有问题或建议，请在GitHub提交Issue或Pull Request。

---

**开始使用：** `python ppt_redesigner.py` 🚀

**最后更新时间：** 2026-05-31
