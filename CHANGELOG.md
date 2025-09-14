# Changelog

All notable changes to claudesidian will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.8.5] - 2025-01-13

### Fixed
- Upgrade command now works without git connection for disconnected users
- Clone latest version to .tmp/ directory instead of requiring upstream remote
- Use .tmp/ instead of /tmp/ to hide upgrade files from Obsidian
- Added user choice prompt when local modifications are detected
- Added verification step to ensure all files were properly addressed
- Added .tmp/ to .gitignore for cleaner repository

## [0.8.4] - 2025-01-13

### Fixed
- Simplified upgrade command to systematically check all system files
- Created upgrade checklist to track progress file-by-file
- Filtered upgrades to only claudesidian system files, not user content
- Added explicit file-by-file diff review before updating
- Made upgrade process resumable with checklist tracking

## [0.8.3] - 2025-01-13

### Fixed
- Improved init-bootstrap vault selection for multiple vaults
- Added explicit confirmation before importing any vault
- Enhanced user identification prompts with better explanations
- Added disambiguation prompts to find the right person when researching
- Clear instructions to never proceed without explicit vault confirmation

## [0.8.2] - 2025-01-13

### Fixed
- Improved SessionStart hook formatting with arrow indicators for commands
- Fixed update notification display to show clean output instead of raw JSON
- Enhanced visual layout of first-run and update messages

## [0.8.1] - 2025-01-13

### Changed
- Updated README with comprehensive feature descriptions including:
  - Smart vault analysis and pattern detection capabilities
  - User research and profile building features
  - Automatic update notification system
  - Web research capabilities with Firecrawl
  - Complete list of available commands including /upgrade

## [0.8.0] - 2025-01-13

### Added
- Automatic update check on session start
- SessionStart hook that fetches latest version from GitHub and compares to local
- Update notifications when newer versions are available
- check-updates npm script for version comparison
- Works even after disconnecting from original repository

### Changed
- Enhanced release command documentation with clearer semantic versioning guidelines
- Better guidance on when to use feat: vs fix: vs refactor: in commits

## [0.7.0] - 2025-01-13

### Added
- Comprehensive vault analysis using tree, note sampling, and pattern detection
- Enhanced profile building with URL fetching and custom context
- Dynamic date generation for timestamps in CLAUDE.md
- "Later" option for Gemini Vision and Firecrawl setup
- Multiple vault import options (yes/no/skip/path)
- Deeper research capabilities with disambiguation confirmation

### Changed
- init-bootstrap now analyzes vault structure before importing
- Always confirms user identity even with single search result
- Waits to create folders until after organization method selection
- Detects plugins and attachments automatically instead of asking
- Firecrawl presented as research game-changer with better explanation
- Profile building includes comprehensive background from provided URLs

### Fixed
- Correct file counting without depth limits
- Proper ordering of import before personalization questions
- More accurate detection of user preferences from existing vault

## [0.6.0] - 2025-01-13

### Added
- Intelligent vault import that preserves existing structure in OLD_VAULT folder
- Auto-detection of existing Obsidian vaults by searching for .obsidian folders
- User research and disambiguation for personalized setup
- Automatic detection of file naming patterns and folder organization
- Vault configuration saved to .claude/vault-config.json for future reference
- Educational explanations during each setup step
- Support for both pnpm and npm package managers
- Comprehensive Obsidian file copying (plugins, trash, settings)
- Clear examples for folder naming when cloning repository

### Changed
- init-bootstrap now imports entire vault structure safely without data loss
- Gemini Vision and Firecrawl prompts clarify tools are already included
- README includes examples of custom folder names when cloning
- Removed unnecessary questions by detecting patterns automatically

## [0.5.0] - 2025-01-13

### Added
- First-run welcome message using SessionStart hook
- FIRST_RUN marker file to detect fresh installations
- Markdown-formatted welcome prompt with setup instructions
- Automatic detection and guidance for new users

### Changed
- init-bootstrap now removes FIRST_RUN marker after setup completion
- Hook configuration uses inline commands (no external scripts needed)

## [0.4.0] - 2025-01-13

### Added
- Simplified setup process with enhanced init-bootstrap command:
  - Automatic disconnection from original repository
  - Folder rename assistance for non-git users
  - Support for both git clone and ZIP download methods
  - Clear prompts for importing existing Obsidian vaults
- Multiple setup paths in README for different user skill levels

### Changed
- init-bootstrap now handles complete environment setup including git management
- README updated with clearer Quick Start instructions for both technical and non-technical users

## [0.3.1] - 2025-01-13

### Fixed
- Removed CLAUDE.md and settings.local.json from repository tracking
- These user-specific files are now generated locally by init-bootstrap
- Added both files to .gitignore to prevent accidental commits
- Clean repository structure for new users

## [0.3.0] - 2025-01-13

### Added
- Intelligent upgrade command (`/upgrade`) with AI-powered semantic merging
- Smart conflict resolution that preserves user customizations while adding new features
- Automatic backup system with rollback capabilities
- Selective update categories (AI-mergeable, auto-safe, protected)
- Based on 2025 best practices for LLM-powered code migration

## [0.2.3] - 2025-01-13

### Changed
- Updated init-bootstrap command and settings configuration

## [0.2.2] - 2025-01-13

### Fixed
- Corrected all documentation to use proper slash command syntax (/command-name)
- Fixed examples showing incorrect 'claude run' syntax
- Updated README, CLAUDE.md, install.sh, and command docs

## [0.2.1] - 2025-01-13

### Changed
- Updated README to use init-bootstrap command instead of install.sh
- Simplified Quick Start instructions to 2-step process
- Added examples of pre-configured commands in README

## [0.2.0] - 2025-01-13

### Added
- Release command for automated version management and releases
- Gemini Vision video analysis support:
  - Local video files (MP4, AVI, MOV, WebM, MKV, WMV, FLV, 3GP, M4V)
  - Direct YouTube URL analysis without download
  - Automatic video processing state detection
- Updated documentation with video analysis examples

### Changed
- Enhanced init-bootstrap command with full environment setup including MCP configuration
- Updated Gemini Vision MCP server to support video formats

## [0.1.0] - 2025-01-13

### Added
- Initial release of claudesidian - Claude Code + Obsidian starter kit
- PARA method folder structure (00_Inbox through 06_Metadata)
- Bootstrap initialization system via `claude run init-bootstrap`
- Pre-configured Claude Code commands:
  - thinking-partner - Collaborative thinking mode
  - inbox-processor - Organize captures
  - research-assistant - Deep dive into topics
  - daily-review - End of day reflection
  - weekly-synthesis - Find patterns in your week
  - create-command - Build new custom commands
  - de-ai-ify - Remove AI writing patterns
  - add-frontmatter - Add metadata to notes
  - init-bootstrap - Interactive setup wizard
- Claude Code agents:
  - thinking-partner agent for exploration and brainstorming
- Helper scripts:
  - firecrawl-batch.sh - Batch web scraping
  - firecrawl-scrape.sh - Single URL scraping
  - fix-renamed-links.js - Fix broken links after renames
  - update-attachment-links.js - Update attachment references
  - transcript-extract.sh - Extract YouTube transcripts
  - vault-stats.sh - Show vault statistics
- Attachment management commands via pnpm
- Gemini Vision MCP server for image/PDF analysis (optional)
- CLAUDE-BOOTSTRAP.md template for configuration
- Comprehensive README with setup instructions
- Install script for automated setup
- Git integration with proper .gitignore

### Changed
- Replaced static CLAUDE.md with dynamic init-bootstrap command

### Security
- API keys stored in environment variables
- .mcp.json gitignored for security

[Unreleased]: https://github.com/heyitsnoah/claudesidian/compare/v0.8.5...HEAD
[0.8.5]: https://github.com/heyitsnoah/claudesidian/compare/v0.8.4...v0.8.5
[0.8.4]: https://github.com/heyitsnoah/claudesidian/compare/v0.8.3...v0.8.4
[0.8.3]: https://github.com/heyitsnoah/claudesidian/compare/v0.8.2...v0.8.3
[0.8.2]: https://github.com/heyitsnoah/claudesidian/compare/v0.8.1...v0.8.2
[0.8.1]: https://github.com/heyitsnoah/claudesidian/compare/v0.8.0...v0.8.1
[0.8.0]: https://github.com/heyitsnoah/claudesidian/compare/v0.7.0...v0.8.0
[0.7.0]: https://github.com/heyitsnoah/claudesidian/compare/v0.6.0...v0.7.0
[0.6.0]: https://github.com/heyitsnoah/claudesidian/compare/v0.5.0...v0.6.0
[0.5.0]: https://github.com/heyitsnoah/claudesidian/compare/v0.4.0...v0.5.0
[0.4.0]: https://github.com/heyitsnoah/claudesidian/compare/v0.3.1...v0.4.0
[0.3.1]: https://github.com/heyitsnoah/claudesidian/compare/v0.3.0...v0.3.1
[0.3.0]: https://github.com/heyitsnoah/claudesidian/compare/v0.2.3...v0.3.0
[0.2.3]: https://github.com/heyitsnoah/claudesidian/compare/v0.2.2...v0.2.3
[0.2.2]: https://github.com/heyitsnoah/claudesidian/compare/v0.2.1...v0.2.2
[0.2.1]: https://github.com/heyitsnoah/claudesidian/compare/v0.2.0...v0.2.1
[0.2.0]: https://github.com/heyitsnoah/claudesidian/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/heyitsnoah/claudesidian/releases/tag/v0.1.0