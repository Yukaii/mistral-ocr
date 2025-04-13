# Mistral OCR PDF 处理工具

这个项目是一个简单但强大的工具，用于使用 Mistral AI 的 OCR (光学字符识别) 功能处理 PDF 文件。该工具能够从 PDF 文档中提取文本内容和图像，并将结果保存为 Markdown 格式。

## 功能特点

- 使用 Mistral AI 的 OCR 能力处理 PDF 文件
- 自动提取文本内容并保留原始布局
- 提取并保存 PDF 中的图像
- 生成包含完整内容的 Markdown 文件
- 支持中文等多种语言

## 安装要求

运行此工具需要以下依赖项：

```bash
pip install mistralai
```

## 使用方法

1. 获取 Mistral AI API 密钥，并在项目根目录创建一个 `.env` 文件，内容例如：
   ```
   MISTRAL_API_KEY=your_mistral_api_key
   ```
2. 指定 PDF 文件路径作为命令行参数运行脚本，可选地使用 `--api-key` 参数覆盖 `.env` 中的 API 密钥。
3. 在终端中运行脚本处理 PDF 文件

```bash
# 在项目根目录创建一个 .env 文件, 内容如下:
MISTRAL_API_KEY=your_mistral_api_key

# 然后运行脚本，传入 PDF 文件路径作为命令行参数
python pdf_ocr.py your_pdf_file.pdf
```

## 输出结果

脚本将在工作目录下创建一个名为 `ocr_results_[PDF文件名]` 的文件夹，其中包含：

- `complete.md`: 包含所有页面内容的 Markdown 文件
- `images/`: 保存 PDF 中提取出的所有图像的文件夹


## 注意事项

- 请确保 PDF 文件路径正确
- API 密钥需要具有 OCR 功能的访问权限


