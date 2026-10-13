# Solgrid Skills

English · [简体中文](README.zh-CN.md)

Reusable skills for agents that turn a concrete creative brief into finished work.

## Improve Video Aesthetics

[Skill instructions](skill/improve-video-aesthetics/SKILL.md) · [Download the skill](improve-video-aesthetics.zip) · [Real example](examples/solar/README.md)

Make visual intent explicit, compare a small number of controlled samples, lock assets, and check whether the style survives motion. The workflow covers lighting, materials, composition, reference use, character/scene consistency and delivery evidence. It is a workflow skill, not a video renderer or a promise of one-click quality.

![Solar explainer before and after](examples/solar/before-after.png)

### Install for Codex

Clone this repository, then copy the skill folder into your skills directory:

```bash
git clone https://github.com/clara-sogreat/solgrid.git
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R solgrid/skill/improve-video-aesthetics "${CODEX_HOME:-$HOME/.codex}/skills/"
```

Alternatively, download the ZIP and extract `improve-video-aesthetics/` into that directory. Other agents that support `SKILL.md` can use the same folder according to their own installation conventions.

### Give your agent a brief

```text
Use $improve-video-aesthetics to improve my 30-second solar explainer.
Keep the scientific explanation and real footage.
Use black silicon, warm gold light and readable physical materials.
First diagnose the current frames, create shared art constraints,
and test one controlled comparison. Then separate still and motion
instructions and review the resulting clips.
For the soundtrack, use soft instrumental piano without voices;
let me hear the music before integrating it.
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

## License

Skill text, configuration and authored documentation: [MIT](LICENSE). Commercial use, modification, redistribution and closed-source use are permitted without a license fee; retain the copyright and license notice. Third-party media, instruments and software retain their own terms; see [NOTICE](NOTICE.md). Installing a skill does not itself authorize paid generation or publication.
