# Changelog

All notable changes to Delphi will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Resume protocol for idempotent re-invocation across sessions
- Discovery file (.discovery.md) for progress tracking
- Flow-by-flow chunking in generate mode
- Priority-tier-per-flow chunking in execute mode
- External evidence storage (evidence/gc-XXX/ directories)
- Incremental report writing in execute mode

### Changed
- Step 5 (Write Output) is now incremental bookkeeping, not batch output
- Evidence referenced by path in reports, never embedded inline
