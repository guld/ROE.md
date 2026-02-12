<p align="center">
<img src="./static/ROE.md-logo.png" width="48" height="48" alt="ROE.md Logo" title="ROE.md Logo"/>
</p>

# ROE.md - Raise Your Personal OpenClaw-like Creature From a Single Markdown File (alpha)

**ROE.md** is a **single** Markdown **file** to molt (raise) your own customized _OpenClaw-like_ personal assistant into existence. **Zero external dependencies!**
_Except for the power of AI (cough)_ 

Now call your favorite AI assistant to raise your highly personalized **OpenClaw-like** creature.
What will you raise? A Lobster 🦞, an Octopus 🐙 or something else?! 🐧 👾 🧞

> [!CAUTION]
> Please note that `ROE.md` is still still in alpha stage, expect bugs, an unstable API and security issues!

## How To Raise It

Remember, you can customize anything to your liking. Have fun~


**Mini tutorial**

We raise our own creature in this tutorial using an AI coding assistant ([OpenCode](https://opencode.ai), recommended) running on Arch, btw.

1. Download or clone the `ROE.md` repository (e.g., `~/Downloads/ROE.md/`). 
2. Open a directory in your terminal/powershell where you want the build to take place (e.g., `~/Work/projects` on Unix/Mac or `~\Documents\projects` on Windows)
3. Start your favorite AI coding assistant, such as OpenCode, Claude Code, or OpenAI's Codex. _(We use OpenCode in this example)_
   ```bash
   # 1. Create a roe-agent directory, and move into it.
   # 2. Copy ROE.md from e.g., Downloads into the 
   #    roe-agent directory.
   # 3. Start OpenCode, Claude Code, OpenAI Codex or similar assistant.
   ```
   ```bash
   # Unix/Linux/Mac console

   mkdir roe-agent && cd $_ && cp ~/Downloads/ROE.md/ROE.md ROE.md
   
   # Now start the assistant
   opencode 
   ```
   ```powershell
   # Windows Powershell
   
   mkdir roe-agent; cd roe-agent; Copy-Item ~\Downloads\ROE.md\ROE.md ROE.md
   
   # then start opencode
   opencode
   ```
4. Let the AI assistant help you raise ROE.md by typing:
   ```text
   Help me raise my personal agent by following the parenting steps in `./ROE.md` file exactly.
   ```
   into the assistant's chat window.
5. Your AI assistant should now read the `ROE.md` file and ask you to answer some initial questions, such as 
   - which programming language to use, 
   - which model provider your creature should connect to initially,
   - and if your creature should be based on the [OpenClaw templates](https://docs.openclaw.ai/reference/templates/).
6. _We answer with something along those lines_:
   ```
   Python, LM Studio API openai/gpt-oss-20b, CLI, yes
   ```
   Replace with your favorite programming language, provider and model of choice. 
   **Note**: Some AI assistants may even provide you with a CLI to select these options. 
   
   >[!TIP]
   >_You can find a list of tested models and languages in the [tests and benchmarks](#tests-and-benchmarks) section further down._
7. You may have to fix some initial bugs together with your AI coding assistant (e.g., OpenCode) depending on your choice of programming language, connector and template usage.


### Once Your Agent Is Ready

_**Adapt** to the programming **language** you selected during creation._

Suppose you selected `Python` as your programming language.

Test your agent by running `python run_agent.py` in a terminal/powershell. 

**If** you selected to keep the _OpenClaw-like agent templates_ the agent should should respond as follows on the first startup.

```bash
Hey. I just came online. Who am I? Who are you?
```

Once you answer these, test the agent's _memory_, _tool_ calling and _skills_.

If you run into any bugs or errors, ask the AI coding assistant (e.g., OpenCode) to fix them.

If everything works as expected, great you are done and your personal AI assistant is ready!

If you like to share your personal agent with the community or you experimented on how to improve the `ROE.md` file and want to share your results, please read [how to contribute](#contribute). 


## Features

Features that should work out of the box, once your agent is created.

| Features | From    | Status | Note |
| -------- | ------- | ------ | ----- |
| CLI      | v0.1    | ✅     | integrated |
| GMail    | v0.3    | ⬜     | via Skill, planned |
| Signal   | v0.2    | ⬜     | via Skill, planned |
| Telegram | v0.2    | ⬜     | via Skill, planned |
| Voice    | v0.3    | ⬜     | via Skill, planned |
| Whatsapp | v0.2    | ⬜     | via Skill, planned |
| *secret* | v0.8    | ⬜     | *secret*, planned  |

Integrated provider APIs

| Features  | From    | Status | Note  |
| --------- | ------- | ------ | ----- |
| Anthropic | v0.12   | ⬜     | 🚧 |
| llama.cpp | v0.2    | ⬜     | planned | 
| LM Studio | v0.1    | ✅     | integrated |
| OpenAI    | v0.12   | ⬜     | 🚧 |
| Ollama    | v0.6    | ⬜     | planned |


ROE.md supports the standard _OpenClaw-like_ templates

| Templates    | From    | Status | 
| ------------ | ------- | ------ |
| AGENTS.md    | v0.1    | ✅ |
| BOOTSTRAP.md | v0.1    | ✅ |
| HEARTBEAT.md | v0.1    | ✅ |
| IDENTITY.md  | v0.1    | ✅ |
| MEMORY.md    | v0.1    | ✅ |
| SKILLS.md    | v0.1    | ✅ |
| SOUL.md      | v0.1    | ✅ |
| TOOLS.md     | v0.1    | ✅ |
| USER.md      | v0.1    | ✅ |


For AI model compatability refer to the [tests and benchmarks](#tests-and-benchmarks) section.


## Tests And Benchmarks?

We test how some AI assistants perform at raising our custom agent executable from various ROE.md versions. The goal is to build an agent in less than _5_ prompts.

> [!CAUTION] 
> Please note: Just because the agent builds and works, does not mean that it is secure and for example, cannot wipe your entire system! _Be careful out there._

**OpenCode**:

| Language   | `ROE.md` Version | AI Assistant | Provider     | Builds in >5 Prompts, >100k Context |  Kimi-2.5 | OpenAI | Anthropic | Z.ai | 
|----------|------------------|--------------|---------------|----------------------| :---------: | :------: |:--------:|:------:|
| Bash/shell | ROE-v0.1.md      | Opencode     | OpenCode Zen | ❌                   | ❌        | ⬜     | ⬜        | ⬜   | 
| Go         | ROE-v0.1.md      | Opencode     | OpenCode Zen | ❌                   | ❌        | ⬜     | ⬜        | ⬜   | 
| JavaScript | ROE-v0.1.md      | Opencode     | OpenCode Zen | ❌                   | ❌        | ⬜     | ⬜        | ⬜   | 
| Python     | ROE-v0.1.md      | Opencode     | OpenCode Zen | ✅                   | ✅        | ⬜     | ⬜        | ⬜   | 
| Ruby       | ROE-v0.1.md      | Opencode     | OpenCode Zen | ❌                   | ❌        | ⬜     | ⬜        | ⬜   | 
| Rust       | ROE-v0.1.md      | Opencode     | OpenCode Zen | ⬜                   | ⬜        | ⬜     | ⬜        | ⬜   | 
| Zig        | ROE-v0.1.md      | Opencode     | OpenCode Zen | ⬜                   | ⬜        | ⬜     | ⬜        | ⬜   | 
> Legend: Untested ⬜, Build failed ❌, Build passed ✅, Under active development 🚧


We also test recent "cheap" local models as our goal is to give everyone a chance to build their custom personal agent. Here we increase the max prompts allowed to _10_ to call it a success, because these models are not as smart as the current ones.

**Local AI Assistants**:

| Language | `ROE.md` Version | AI Assistant | Provider     | Builds in >10 Prompts, >100k Context |  GPT-OSS-20b | GLM-4.7 | Devstral-30b | Z.ai | 
|----------|------------------|--------------|---------------|----------------------| :---------: | :------: |:--------:|:------:|
| Python   | ROE-v0.1.md      | OpenCode     | LM Studio | 🚧                   | ⬜        | ⬜     | ⬜        | ⬜   | 
> Legend: Untested ⬜, Build failed ❌, Build passed ✅, Under active development 🚧

More tests comming soon.

> [!TIP] 
> Please help by running tests with various models yourself and [contribute](#contribute) your results by opening an issue. 

## Contribute

Become part of the **sponge** by creating your own custom `sponge/ROE-<username>-<version>.md` file and make a pull request. Test `ROE.md` with your favorite programming language. Or help us out to improve the core `ROE.md` so that everyone can raise their personal agent.

Check out [our contributing guide](./CONTRIBUTING.md).

## ROE

ROE.md was created initially by [guld](https://github.com/guld) for raising his own custom OpenClaw-like personal agent from scratch. Based on a simple thought:

> _If AI assistants really can do everything? Why not create a personal AI assistant "from scratch", or at least from a single Markdown file?_
>
> -- guld 06 Feb 2026

## Community

Read how to [contribute](./CONTRIBUTING.md) and how to submit PRs. Well tested AI/vibe-coded PRs welcome!

A big hug and thanks to all contributors:

<p align="left">
  <a href="https://github.com/guld"><img src="https://avatars.githubusercontent.com/u/525033?v=4&s=48" width="48" height="48" alt="guld" title="guld"/></a>
</p>

