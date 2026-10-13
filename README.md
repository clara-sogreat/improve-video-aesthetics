
# Improve Video Aesthetics

English · [简体中文](README.zh-CN.md)

Reusable agent skills for creators worldwide: turn a concrete creative brief into finished work. English is the default documentation and skill language; Simplified Chinese documentation and bilingual quick-start examples are also available.

## Improve Video Aesthetics

[Skill instructions](skill/improve-video-aesthetics/SKILL.md) · [Download the skill](improve-video-aesthetics.zip) · [Real example](examples/solar/README.md)

Make visual intent explicit, compare a small number of controlled samples, lock assets, and check whether the style survives motion. The workflow covers lighting, materials, composition, reference use, character/scene consistency and delivery evidence. It is a workflow skill, not a video renderer or a promise of one-click quality.

![Solar explainer before and after](examples/solar/before-after.png)

### Use cases and OpenMontage

Apply the workflow to product promos, launch videos, branded shorts and explainers. Pair it with [OpenMontage](https://github.com/calesthio/OpenMontage) for video production: use this skill to define and review the art direction, and OpenMontage to assemble and render the film. The included solar film demonstrates that pairing; the other use cases are suggested applications, not measured benchmarks.

### Install for Codex

Clone this repository, then copy the skill folder into your skills directory:

```bash
# Clone the repository / 克隆仓库
git clone https://github.com/clara-sogreat/improve-video-aesthetics.git
# Create your skills directory / 创建技能目录
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
# Install the skill / 安装技能
cp -R improve-video-aesthetics/skill/improve-video-aesthetics "${CODEX_HOME:-$HOME/.codex}/skills/"
```

Alternatively, download the ZIP and extract `improve-video-aesthetics/` into that directory. Other agents that support `SKILL.md` can use the same folder according to their own installation conventions.

### Give your agent a brief

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


### What it delivers

- A diagnosis grounded in available frames or footage.
- Shared art constraints and a controlled comparison record.
- Asset prompts and separate still/motion briefs.
- A continuity and delivery checklist, with verified and unverified results separated.

Use available tools; no Midjourney account, proprietary profile ID or bundled paid service is required. Provider-specific generation, pricing and licensing depend on your chosen tools and must be checked when used.

## Example and provenance

The solar example uses locally authored Blender illustrations and licensed real footage, assembled with [OpenMontage](https://github.com/calesthio/OpenMontage). It demonstrates this workflow in an actual production. The final piano accompaniment is an original instrument-rendered arrangement; it is not a successful HeartMuLa no-vocal generation.

[Example notes and credits](examples/solar/README.md) explain the controlled lighting test and the limits of the before/after comparison. The original tutorial that informed the method is not redistributed; [method notes](skill/improve-video-aesthetics/references/video-notes.md) distinguish paraphrased tutorial methods from added workflow guidance.

## Contributing

Contributions from any region are welcome. Keep reusable skill instructions and configuration in English, provide bilingual quick-start examples, and keep translations aligned with the English documentation. Include observable evidence and clearly identify pending checks; do not submit credentials, personal paths or assets you cannot redistribute.

## License

Skill text, configuration and authored documentation: [MIT](LICENSE). Commercial use, modification, redistribution and closed-source use are permitted without a license fee; retain the copyright and license notice. Third-party media, instruments and software retain their own terms; see [NOTICE](NOTICE.md). Installing a skill does not itself authorize paid generation or publication.
