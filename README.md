# caganme

A Claude Code skill that answers product questions from the work of Marty Cagan and SVPG, with sources.

I use it to test my product strategy, my interview answers and my home assignments.

## How it works

It has three levels, from fast to deep:

1. `skill/SKILL.md` holds a short summary of the main ideas and the answer modes (Ask, Critique, Grade, Pushback). It answers most questions without a search.
2. `skill/doctrine/*.md` are 10 reading lists, one for each topic (strategy, discovery, teams, the AI era and more). Each list gives the best articles first, with links.
3. `agents/svpg-researcher.md` is a sub-agent that searches the full local collection and returns a short brief with citations. The search runs in its own context, so long search results do not fill the main conversation.

There is no vector database. With about 500 articles and very consistent words, a plain text search (grep) works well and needs no extra system.

## The collection is not included

The skill expects a local folder `~/svpg-corpus/` with the articles as Markdown files (481 articles and podcast transcripts in my copy). The articles are SVPG's copyrighted work, so this repository has only the skill, the agent and the reading lists with links.

## Install

1. Copy `skill/` to `~/.claude/skills/caganme/`.
2. Copy `agents/svpg-researcher.md` to `~/.claude/agents/`.
3. In Claude Code, type `/caganme` and your question.

Built with Claude Code.
