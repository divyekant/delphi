# Changelog

All notable changes to Delphi will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.0.0] - 2026-02-27

### Added
- Skill definition with frontmatter, overview, mode detection, and guided case format
- Generate mode: context gathering, surface discovery, case generation with coverage matrix
- Execute mode: case loading, browser/API/CLI execution, evidence capture, reporting
- Resume protocol for idempotent re-invocation across sessions
- Discovery file (.discovery.md) for progress tracking
- Flow-by-flow chunking in generate mode with parallel subagent dispatch
- Priority-tier-per-flow chunking in execute mode
- Parallel subagent dispatch for execute mode (non-UI flows run concurrently)
- Flow classification: UI flows sequential, API/CLI/background flows parallel
- Report fragment merge from parallel subagents
- External evidence storage (evidence/gc-XXX/ directories)
- Incremental report writing in execute mode
- Reference guided case examples for positive and negative paths
- LLM quickstart guide for pasting into any LLM context
- OSS scaffolding: MIT license, contributing guide, code of conduct
- Apollo project configuration

### Changed
- Step 5 (Write Output) is now incremental bookkeeping, not batch output
- Evidence referenced by path in reports, never embedded inline
