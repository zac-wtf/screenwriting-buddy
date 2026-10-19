# 剧本创作搭子

一个面向抖音独立剧情短片与连续短剧的中文 Codex skill。

你提供核心创意，搭子通过一次一个关键问题，和你一起推演、写稿、诊断与修改。观看吸引力优先，创作方向和最终审核由你掌握。

## 它怎样与你合作

- **先问关键问题**：一次只问一个影响方向的决策，给出推荐和理由，不重复询问已知信息。
- **主动提出异议**：说明哪里不成立、会怎样影响观看，再提出可行改法。
- **尽早动笔**：核心事件、观看期待和结尾兑现方向清楚后就写，细节在写作中补足。
- **从观看过程审稿**：检查观众为什么留下、在等什么、获得什么、哪里可能失去兴趣。
- **先诊断再修改**：收到“不好看”时，先定位具体段落的问题，必要时追问一个关键点。
- **保留人的决定权**：允许大胆设定和强冲突，人物动机与规则要连贯；所有成稿交由人工最终审核。

适用于剧情创意、大纲、独立短片、连续短剧、场景与对白修改。普通文章、知识口播、纯广告文案和视频生成执行不属于它的主要用途。

## 安装到 Codex

### 在对话中安装

把下面这句话发送给支持 skill 安装的 Codex：

> 请使用 skill-installer，从 GitHub 仓库 zac-wtf/screenwriting-buddy 的 skills/screenwriting-buddy 目录安装「剧本创作搭子」。

安装后的调用名是 `$screenwriting-buddy`。在下一轮对话中调用；若界面尚未刷新，可新开一段对话。

### 手动安装

1. 在 [Releases](https://github.com/zac-wtf/screenwriting-buddy/releases) 下载 `screenwriting-buddy.skill`。
2. 这个文件是 ZIP 格式的技能包。若解压工具不识别 `.skill`，先将扩展名改为 `.zip`，再解压。
3. 将解压得到的整个 `screenwriting-buddy` 文件夹放入 Codex 的技能目录，默认是 `~/.codex/skills/`；自定义了 `CODEX_HOME` 时，放入其 `skills/` 子目录。
4. 确认文件结构为 `skills/screenwriting-buddy/SKILL.md`，而非额外嵌套两层同名目录。在下一轮对话调用。

如已安装同名技能，先备份旧版本再替换。技能目录中的文件应来自你信任的来源，可以先直接阅读 [SKILL.md](skills/screenwriting-buddy/SKILL.md)。

## 怎么用

### 从一个点子开始

```text
用 $screenwriting-buddy 和我一起发展这个抖音剧情创意：
一个能听见物品抱怨的维修工，接到了一件始终不肯说话的旧物。
先问一个影响故事方向的关键问题，并给出你的建议。
```

### 修改已有剧本

```text
用 $screenwriting-buddy 审读下面这版剧本。
优先检查观众为什么愿意看完，指出对应段落和原因，先不要重写全稿。
【粘贴剧本】
```

### 收到模糊反馈

```text
用 $screenwriting-buddy 和我一起修改这场戏。
目前我觉得不好看，先诊断问题，必要时只问我一个关键点，再给出修改。
【粘贴场景】
```

题材、时长、必须保留的内容和结局如果已经确定，可以一并提供。也可以直接说“你定”或“先写一版”，搭子会按已有信息推进。

## 文件结构

```text
skills/screenwriting-buddy/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── story-development.md
    ├── scene-dialogue.md
    └── viewer-review.md
```

三个参考文件分别处理故事推演、场景对白、观看过程与反馈诊断，按任务读取。

本技能可独立使用。文中提到的 `screenwriting`、`human-writing`、`humanizer-zh` 等是可选的已有方法入口，不是安装依赖，也没有打包在本仓库中。

## 反馈与改进

欢迎通过 [Issues](https://github.com/zac-wtf/screenwriting-buddy/issues) 提交使用反馈。提供任务类型、期望行为和实际问题，有助于定位改进点；示例请使用你有权分享的材料。

本技能提供创作建议，不承诺播放量、完播率或爆款结果。真实受众反馈和人工审核是后续修改的依据。
