# 代码审计报告

此目录包含自动生成的代码审计报告。

## 📋 报告说明

- `code-audit-report-latest.md` - 最新的代码审计报告
- `code-audit-report-YYYYMMDD.md` - 按日期保存的历史报告

## 🔄 自动生成

报告由 GitHub Actions 自动生成：
- **定时执行**：每天 UTC 时间 02:00（北京时间 10:00）
- **手动触发**：可在 GitHub Actions 页面手动触发

## 📊 报告内容

报告包含以下内容：

1. **总体统计**
   - 总文件数、代码行数
   - 有效代码行数、空行数
   - 平均圈复杂度、最大圈复杂度

2. **进程分类统计**
   - 主进程（main）和渲染进程（renderer）的代码分布
   - 各进程的代码量占比和对比

3. **语言占比统计**
   - 各编程语言的代码量占比
   - 各语言的文件数量对比

4. **圈复杂度分析**
   - 复杂度分布情况
   - 高复杂度文件列表（Top 10）

5. **进程多维度分析**
   - 雷达图展示各进程的多维度特征

6. **Git 提交分析**（近半年）
   - 提交代码变更趋势
   - 提交影响分析
   - 贡献者提交分布
   - 提交频率分析

7. **时间段改动量占比分析**
   - 不同时间段（近一周、近一月、近一季、近半年、近一年、所有时间）的代码改动量
   - 净变化量和占比

8. **NPM 依赖项分析**
   - 依赖项类型对比
   - 依赖项作用域分布
   - 版本前缀分布

## 📁 查看报告

报告保存在 **MetaDoc-Releases** 仓库的 `reports/code-audit/` 目录下：

- **最新报告**：在 MetaDoc-Releases 仓库的 `reports/code-audit/code-audit-report-latest.md`
- **历史报告**：查看对应日期的报告文件（格式：`code-audit-report-YYYYMMDD.md`）
- **GitHub Issue**：每次生成报告后会在当前仓库（MetaDoc）自动创建或更新 Issue
- **Artifact**：在 GitHub Actions 运行页面可下载报告 Artifact

## 🔧 手动运行

如果需要手动生成报告，可以在项目根目录运行：

```bash
cd meta-doc
npm run audit
```

报告将生成在 `meta-doc/code-audit-report.md`。

