# 闪卡学习系统

一个基于JSON数据的在线闪卡学习平台，支持多书籍、多章节的单词学习。

## 功能特点

- 📚 **多书籍支持**：支持多个JSON书籍文件
- 📖 **章节选择**：每个书籍包含多个章节
- 🎯 **随机选项**：4个选项随机排序，提升学习效果
- 📊 **进度跟踪**：实时显示学习进度和得分
- 💬 **例句强调**：突出的例句显示，便于理解
- ℹ️ **单词解释**：点击查看详细的单词解释（支持Markdown）
- 🔄 **自由导航**：支持上一题/下一题切换
- 📱 **响应式设计**：支持桌面端和移动端

## 项目结构

```
flashcard_new/
├── index.html          # 主页面
├── books/              # 书籍数据目录
│   └── word1.json      # 示例书籍数据
└── README.md           # 项目说明文档
```

## 数据格式

### JSON文件结构

```json
{
    "book_name": "书籍名称",
    "chapters": [
        {
            "chapters_name": "章节名称",
            "words": [
                {
                    "id": 1,
                    "word": "单词",
                    "sentence": "例句",
                    "translation": "正确翻译",
                    "confused_answer_1": "错误选项1",
                    "confused_answer_2": "错误选项2",
                    "confused_answer_3": "错误选项3",
                    "explanation": "# 单词解释\n\n**词性**：名词\n\n**含义**：..."
                }
            ]
        }
    ]
}
```

### 字段说明

- `book_name`: 书籍名称
- `chapters_name`: 章节名称
- `word`: 单词
- `sentence`: 例句
- `translation`: 正确翻译
- `confused_answer_1/2/3`: 错误翻译选项
- `explanation`: 单词解释（支持Markdown格式）

## 使用方法

### 1. 直接使用

1. 下载项目文件
2. 确保JSON文件放在 `books/` 目录下
3. 用浏览器打开 `index.html`
4. 选择书籍和章节开始学习

### 2. 本地服务器

```bash
# 进入项目目录
cd flashcard_new

# 启动本地服务器（Python 3）
python -m http.server 8000

# 访问 http://localhost:8000
```

### 3. 添加新书籍

1. 在 `books/` 目录下创建新的JSON文件
2. 按照上述数据格式编写内容
3. 刷新页面即可自动加载新书籍

## 操作说明

1. **选择书籍**：在顶部下拉框选择要学习的书籍
2. **选择章节**：选择具体的章节开始练习
3. **答题**：点击4个选项中的一个进行答题
4. **查看解释**：点击单词右侧的ℹ️按钮查看详细解释
5. **导航**：使用上一题/下一题按钮切换题目
6. **查看进度**：底部显示当前进度和得分

## 技术栈

- **前端**：HTML5, CSS3, JavaScript (ES6+)
- **样式**：CSS Grid, Flexbox, CSS动画
- **数据处理**：JSON, Fetch API
- **特殊功能**：Markdown渲染

## 浏览器兼容性

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 开发说明

### 添加新功能

项目采用模块化设计，主要功能模块：

- `loadBooks()`: 加载书籍数据
- `startPractice()`: 开始练习
- `showQuestion()`: 显示题目
- `selectOption()`: 处理答题
- `toggleExplanation()`: 切换单词解释

### 样式定制

主要CSS类：

- `.container`: 主容器
- `.header`: 顶部导航
- `.word-row`: 单词行
- `.sentence`: 例句
- `.options`: 选项区域
- `.explanation-panel`: 解释面板

## 许可证

MIT License

## 贡献

欢迎提交Issue和Pull Request来改进这个项目！

## 联系方式

如有问题或建议，请通过以下方式联系：

- GitHub Issues
- Email: [your-email@example.com]

---

**Happy Learning! 🎓**