# My templates for LLM
Use these with LLM 0.24a0 or later and the [llm-templates-github](https://github.com/simonw/llm-templates-github) plugin.

## Setup

```bash
brew install llm
```

install that plugin like this:

```bash
llm install llm-templates-github
```

## Usage

### Simple summarize

```bash
curl -sL 'https://llm.datasette.io/' | llm -t gh:John-Lin/summarize -p language English
```

#### template parameters:
- language: the language to use for the output, e.g. `English`, `French`, `Spanish`, etc.

### Meta prompt summarize

```bash
complex_prompt=$(llm -t gh:John-Lin/meta_prompt_summarize -p language English)

llm -f https://www.bbc.com/sport/football/articles/crl05r070wro -s $complex_prompt
```

#### template parameters:

- language: the language to use for the output, e.g. `English`, `French`, `Spanish`, etc.
- simple_prompt: a simple prompt to use for LLM to improve prompts e.g. `Summarize this article in one sentence.`

## References
- [Meta prompts](https://cookbook.openai.com/examples/enhance_your_prompts_with_meta_prompting)
- [Prompt generation](https://platform.openai.com/docs/guides/prompt-generation?context=text-out)
