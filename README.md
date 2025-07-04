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

simple summarize of a web page:

```bash
curl -sL 'https://llm.datasette.io/' | llm -t gh:John-Lin/summarize
```

meta prompt summarize a news article:

```bash
complex_prompt=$(llm -t gh:John-Lin/meta_prompt_summarize)

llm -f https://www.bbc.com/sport/football/articles/crl05r070wro -s $complex_prompt
```
