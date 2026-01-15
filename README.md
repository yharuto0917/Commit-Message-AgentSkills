# Commit Message Skill 📝

[日本語 (Japanese)](./READMEjp.md)

A comprehensive Claude Code skill for creating effective and readable commit messages. Supports multiple conventions including Conventional Commits, Semantic Commits, and Japanese practices.

## 🌟 Features

- **Auto-generation**: Generate commit messages from `git diff` and `git status`
- **Multiple Conventions**: Support for Conventional Commits, Semantic Commits, and Japanese practices
- **Validation**: Check existing messages against conventions
- **Best Practices**: Provide guidelines and templates for various scenarios
- **Japanese Support**: Full Japanese language support for commit messages

## 📦 Installation

### 🤖 For Claude Code Users

1. **Download the skill package**
   ```bash
   # Download commit-message.skill file
   ```

2. **Install using Claude Code CLI**
   ```bash
   claude skills install commit-message.skill
   ```

3. **Start using**
   - Ask Claude: "Create a commit message"
   - Claude will automatically use this skill to generate messages

### 💎 Alternative Manual Installation

1. **Extract the skill**
   ```bash
   unzip commit-message.skill -d ~/.claude/skills/commit-message
   ```

2. **Verify installation**
   ```bash
   claude skills list
   ```

## 🎯 Supported Conventions

### Conventional Commits
International standard convention widely used in open source projects.

**Format:**
```
<type>[optional scope]: <description>

[optional body]

[optional footer]
```

**Example:**
```
feat(auth): add two-factor authentication

Implement SMS-based 2FA.
Send one-time code during login.

Closes #123
```

### Semantic Commits
More intuitive verb-based convention.

**Format:**
```
<verb>: <subject>

[optional body]
```

**Example:**
```
add: user profile customization feature

Allow users to customize their profile appearance
with themes and layout options.
```

### Japanese Practices
Japanese-friendly commit message convention.

**Format:**
```
<動詞>：<対象>

[詳細説明]
```

**Example:**
```
追加：ダークモード機能

ヘッダーにダークモード切り替えボタンを追加。
ユーザーの設定はlocalStorageに保存。

Closes #456
```

## 🚀 Usage

### Generate Commit Message

Simply ask Claude:
```
"Create a commit message"
"Help me write a commit"
"Generate commit message from my changes"
```

Claude will:
1. Run `git status` and `git diff --staged`
2. Analyze your changes
3. Detect project conventions
4. Generate an appropriate message

### Validate Existing Message

Ask Claude to review:
```
"Check this commit message"
"Review my commit message"
"Is this commit message good?"
```

Claude will:
1. Read your message
2. Identify the convention used
3. Validate against rules
4. Suggest improvements

### Get Best Practices

Ask for guidance:
```
"How to write good commit messages?"
"What should I include in commit body?"
"Show me commit message templates"
```

## 📚 Included Resources

### Reference Files (All in Japanese)

- **conventional_commits.md**: Complete guide to Conventional Commits
- **semantic_commits.md**: Semantic Commits specification
- **japanese_practices.md**: Japanese commit message practices
- **best_practices.md**: 7 golden rules and best practices
- **templates.md**: Templates for various scenarios

### Covered Scenarios

- New features (small, medium, large)
- Bug fixes (simple, detailed, hotfix)
- Refactoring
- Performance improvements
- Documentation updates
- Tests
- Breaking changes
- Reverts

## 💡 Examples

### Example 1: Feature Addition

**Your changes:**
- Added dark mode toggle
- Updated theme system
- Added localStorage persistence

**Generated message:**
```
feat: add dark mode feature

Add dark mode toggle button in header.
User preferences are saved to localStorage
and persist across sessions.

Implementation:
- ThemeProvider for app-wide theme management
- ThemeToggle component for UI
- Auto-detection of system preferences

Closes #456
```

### Example 2: Bug Fix

**Your changes:**
- Fixed session timeout logic
- Updated error handling

**Generated message:**
```
fix: session timeout error on login

Session validity check logic was incorrect,
causing timeout errors even for valid sessions.

Updated validation logic to properly check
expiration timestamps.

Fixes #789
```

### Example 3: Japanese Message

**Your changes:**
- Refactored authentication logic
- Split into multiple modules

**Generated message:**
```
リファクタリング：認証ロジックの整理

【背景】
認証コードが複数ファイルに散在し、
メンテナンスが困難になっていた。

【変更内容】
1. AuthServiceクラスに処理を集約
2. JWT処理をTokenManagerに分離
3. セッション管理をSessionStoreに分離

【保証】
全テストが通過。外部動作は完全に同一。
```

## 🎨 Convention Detection

The skill automatically detects your project's convention by:

1. Checking for `.commitlintrc` or `commitlint.config.js`
2. Analyzing recent commit history (`git log --oneline -20`)
3. Identifying patterns:
   - `feat:`, `fix:` → Conventional Commits
   - `add:`, `update:` → Semantic Commits
   - Japanese verbs → Japanese practices

## ✨ Key Benefits

- **Consistency**: Unified conventions across the project
- **Readability**: Easy to understand history
- **Efficiency**: Faster code reviews and debugging
- **Automation**: Enable automatic CHANGELOG generation
- **Team collaboration**: Better communication through clear messages

## 📖 Documentation

Full documentation is included in the skill's reference files:

- Detailed explanations of each convention
- Step-by-step guides for writing messages
- Common mistakes and how to avoid them
- Team convention setup guidelines
- Tool integration (commitlint, husky)

## 🤝 Contributing

This skill was created following the Claude Code Skill Creator guidelines. Feedback and suggestions are welcome!

## 📄 License

This skill is provided as-is for use with Claude Code.

---

**Made with ❤️ for better commit messages**
