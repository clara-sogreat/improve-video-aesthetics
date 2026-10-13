# Solgrid Skills

[English](README.md) · 简体中文

面向全球创作者的可复用 AI Agent 技能，把具体创作需求转化为可检查、可交付的作品。英文是默认文档与技能语言，同时提供简体中文说明和中英双语快速开始示例。

## AI 视频美术质量提升

[技能说明（英文）](skill/improve-video-aesthetics/SKILL.md) · [下载技能包](improve-video-aesthetics.zip) · [实际制作案例](examples/solar/README.md)

把“科技感、电影感、震撼”转化为明确的光色、材质、构图与镜头规则。先用少量固定内容小样比较风格，再锁定资产，检查美术风格是否能延续到动态画面。

![太阳能短片提升前后](examples/solar/before-after.png)

### 使用场景与 OpenMontage

适用于商品宣传片、产品发布短片、品牌短视频和科普解说。建议配合 [OpenMontage](https://github.com/calesthio/OpenMontage)：本技能负责制定和检查美术方向，OpenMontage 负责视频合成与渲染。仓库中的太阳能短片展示了这一组合；其他场景属于可尝试的应用，不代表已完成效果基准测试。

### 安装与使用

克隆仓库并安装到 Codex 的技能目录：

```bash
# Clone the repository / 克隆仓库
git clone https://github.com/clara-sogreat/solgrid.git
# Create your skills directory / 创建技能目录
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
# Install the skill / 安装技能
cp -R solgrid/skill/improve-video-aesthetics "${CODEX_HOME:-$HOME/.codex}/skills/"
```

也可下载 ZIP，把其中的 `improve-video-aesthetics/` 文件夹放进技能目录。支持 `SKILL.md` 的其他 agent 可按各自约定使用。

给 agent 提供脚本、当前画面、参考、画幅、时长和预算。下面两份委托语含义一致，可直接复制任一版本：

English / 英文：

```text
Use OpenMontage with $improve-video-aesthetics to improve my 30-second solar explainer.
Keep the scientific explanation and real footage.
Use black silicon, warm gold light and readable physical materials.
First diagnose the current frames, define shared art constraints,
and test one controlled comparison. Then separate still and motion
instructions and review the resulting clips.
Use soft instrumental piano without voices; let me hear it before integration.
```

简体中文 / Simplified Chinese：

```text
将 OpenMontage 与 $improve-video-aesthetics 配合使用，提升我的 30 秒太阳能短片。
保留科学解释与实拍素材，采用深黑硅晶、暖金光和清晰的物理材质。
先诊断当前画面，制定共用美术约束，做一次固定内容对比。
再分别编写静帧与运动指令，并检查实际生成片段。
配乐使用轻柔纯器乐钢琴，先让我试听再集成。
```

### 可以得到什么

- 基于现有证据的质量诊断与优先修正项。
- 共用美术约束卡和固定内容对比记录。
- 角色、场景资产提示词及分开的静帧／运动分镜。
- 连续性与成片检查，明确通过、失败及待验证项。

技能不绑定付费工具或私人审美配置。它提供制作方法，不保证一键提升效果；具体生成工具的费用、能力与素材授权需按实际使用确认。

### 实际案例与来源

太阳能案例使用自行制作的 Blender 示意画面和有授权的实拍素材，通过 [OpenMontage](https://github.com/calesthio/OpenMontage) 合成。最终配乐是原创器乐编排，不是 HeartMuLa 成功生成无人声的案例。

[案例说明与来源](examples/solar/README.md) 区分固定灯光对比和多因素改动的前后展示；后者不属于因果效果基准。技能方法由参考教程提炼并补充实践检查，不包含原作者教程文件、私人配置或原作者技能包。

### 贡献

欢迎全球创作者提交有具体画面证据的改进。可复用技能正文与配置统一使用英文；快速开始示例提供中英双语，翻译与英文主文档保持一致。说明使用条件、实际观察、失败与待验证部分；请勿提交个人路径、凭据、模型权重或无权分发的素材。

### 开源协议

技能文字、配置和自行编写的文档采用 [MIT](LICENSE)：允许免费商用、修改、分发和闭源使用，保留版权和许可声明即可。第三方素材、乐器采样与软件保留各自条款，见 [NOTICE](NOTICE.md)。
