# GPT-3 PDF 翻译工具

此工具使用PyPDF2 从 PDF 中提取文本，并使用 OpenAI GPT-3 API 进行翻译。如果您有多个 OpenAI API 密钥，该工具将在它们之间进行切换，分布请求。翻译后的文本将保存在用户的桌面上作为一个文本文件。

## 要求
- Python 3
- PyPDF2
- OpenAI 的 Python 客户端

## 安装

1. 克隆仓库：
   ```bash
   git clone https://github.com/你的github用户名/pdf-translator-gpt3.git
   ```

2. 导航到克隆的目录：
   ```bash
   cd pdf-translator-gpt3
   ```

3. 安装必要的库：
   ```bash
   pip install PyPDF2 openai
   ```

## 配置

在使用工具之前，您需要进行一些配置：

- `API_KEYS`：您的 OpenAI API 密钥列表。
- `path`：您要翻译的 PDF 文件的路径。
- `ori_prompt`：用于 GPT-3 的原始提示，例如 "将以下英文文本翻译成中文："。

在 `config.py` 文件中设置上述变量。

## 使用方法

运行主脚本：

```bash
python main.py
```

该工具将从指定的 PDF 中提取文本，将其分割成易于管理的块，然后使用 GPT-3 进行翻译。翻译后的文本将保存到您桌面上的文本文件中。

## 特点

- **PDF 文本提取**：使用 PyPDF2 从 PDF 文件中提取文本内容。
- **API 密钥轮换**：在多个 OpenAI API 密钥之间有效地切换。
- **多线程**：通过同时翻译多个块来加速翻译过程，每次都会预测并修改合适的线程数。

## 贡献

随时欢迎提出问题和改进建议！

## 鸣谢
该README文档由chatGPT-4创建。

## 许可

此项目是开源的，遵循 [MIT License](LICENSE)。
