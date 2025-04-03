# Ask the Document

## 简介
"Ask the Document" 是一个基于 LangChain 和 Google Gemini 模型的交互式文档问答应用程序。它允许用户上传 PDF、DOCX 或 TXT 格式的文档，并通过自然语言与这些文档进行交互，获取相关信息。该应用程序利用了向量数据库和检索增强生成（RAG）技术，能够根据用户的问题从文档中检索相关内容，并生成简洁的答案。

## 功能特性
- **多格式支持**：支持上传 PDF、DOCX 和 TXT 格式的文档。
- **历史对话感知**：能够理解用户的问题，并结合历史对话提供更准确的答案。
- **简洁回答**：生成的答案简洁明了，最多不超过三句话。
- **流式响应**：在回答问题时提供流式响应，增强用户体验。

## 安装与使用

### 环境要求
- Python 3.8 或更高版本
- 所需的 Python 库可以通过 `pip` 安装，具体依赖项可以在代码中查看。

### 安装步骤
1. **克隆仓库**：
```bash
git clone <your-github-repo-url>
cd <your-repo-directory>
```
2. **创建虚拟环境**：
```bash
python -m venv venv
source venv/bin/activate  # 对于 Windows 用户，使用 `venv\Scripts\activate`
```
3. **安装依赖项**：
```bash
pip install -r requirements.txt  # 如果有 requirements.txt 文件
```
4. **设置环境变量**：
在项目根目录下创建一个 `.env` 文件，并添加以下内容：
```plaintext
GOOGLE_GEMINI_KEY=your_google_gemini_api_key
```
将 `your_google_gemini_api_key` 替换为你自己的 Google Gemini API 密钥。

### 使用步骤
1. **运行应用程序**：
```bash
streamlit run langchain.py
```
2. **上传文档**：
在应用程序界面中，点击 "Upload your document: " 上传你想要查询的文档，然后点击 "Submit File" 按钮。
3. **提问**：
在聊天输入框中输入你的问题，应用程序将根据文档内容提供相应的答案。

## 代码结构
- `langchain.py`：主应用程序文件，包含了文档处理、向量存储、检索链和对话链的创建，以及用户界面的实现。

## 注意事项
- 请确保你已经正确设置了 Google Gemini API 密钥，否则应用程序将无法正常工作。
- 目前仅支持 PDF、DOCX 和 TXT 格式的文档，其他格式的文档将无法处理。

## 贡献
如果你想为这个项目做出贡献，请遵循以下步骤：
1. **Fork 仓库**：在 GitHub 上 Fork 这个项目到你自己的仓库。
2. **创建新分支**：在你的本地仓库中创建一个新的分支，用于开发新功能或修复问题。
3. **提交代码**：在完成开发后，将你的代码提交到你的 Fork 仓库，并创建一个 Pull Request。

## 许可证
本项目采用 [MIT 许可证](https://opensource.org/licenses/MIT)。

## 联系方式
如果你有任何问题或建议，请随时通过 GitHub Issues 与我联系。
