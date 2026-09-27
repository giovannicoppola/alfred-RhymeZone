# RhymeZone 🎵

An [Alfred](https://www.alfredapp.com/) workflow to find rhymes for a word, with syllable
counts, from the [Datamuse API](https://www.datamuse.com/api/) — the engine behind
[RhymeZone](https://www.rhymezone.com).

<a href="https://github.com/giovannicoppola/alfred-RhymeZone/releases/latest/">
<img alt="Downloads"
src="https://img.shields.io/github/downloads/giovannicoppola/alfred-RhymeZone/total?color=purple&label=Downloads"><br/>
</a>

## Installation

Download the latest `.alfredworkflow` from [Releases](https://github.com/giovannicoppola/alfred-RhymeZone/releases/latest)
and double-click it. Requires Alfred with the Powerpack and an internet connection; there is
nothing else to install.

## Usage

Type `rhy` followed by a word, e.g. `rhy time`. Rhymes are listed best match first, each
with its syllable count and Datamuse score.

- <kbd>↩</kbd> copy the word
- <kbd>⌘</kbd><kbd>L</kbd> show it in Large Type
- <kbd>⇧</kbd> or <kbd>⌘</kbd><kbd>Y</kbd> preview the word on RhymeZone

The search waits until you stop typing, so Datamuse isn't queried on every keystroke.

## Background

Written in response to a request on the Alfred Forum: [Workflow for rhymes](https://www.alfredforum.com/topic/22849-workflow-for-rhymes).

# Changelog
- 2026-09-27: version 0.1.0, no dependencies: rewritten in JavaScript for Automation (no more
  `jq`, which older macOS versions lack), 5-second network timeout and a clear message when
  Datamuse can't be reached, RhymeZone preview, waits for typing to pause
- 2026-07-21: version 0.0.2, URL-encode the query, build the JSON with jq (escape-safe), fewer
  processes, prompt-on-empty and friendly no-results
