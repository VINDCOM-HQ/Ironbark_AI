# Changelog

All notable changes to Ironbark will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

---

## [Unreleased]

### Added
- **Microsoft Teams bot** &mdash; conversational AI in channels and DMs with code generation
- **Slack bot** &mdash; threaded conversations, slash commands, and syntax-highlighted code snippets
- **Discord bot** &mdash; server-based AI assistant with role-based access and thread awareness
- All messaging integrations inherit RBAC policies, model restrictions, and audit trail from Admin Console
- Desktop app (Tauri v2) for macOS, Linux, and Windows
- VS Code extension for inline AI assistance
- Per-tool RBAC for SAST MCP providers (Checkmarx, Semgrep, Sonatype)
- Documentation MCP providers (Confluence, Notion, SharePoint) via admin-managed proxy
- License activation server for enrollment and seat management
- Session sharing and export capabilities
- User hooks for custom pre/post tool execution workflows
- Managed commands, skills, and formatters configurable from Admin Console
- Token usage tracking with daily aggregation and per-model cost breakdowns
- Web search policy configuration
- LSP (Language Server Protocol) integration for real-time diagnostics

### Changed
- Admin Console Docker image renamed to `vindcom/ironbark-admin-console`
- Surfaces badge updated to reflect all 9 platform surfaces

---

## [0.1.0] - Initial Release

### Added
- Admin Console with fleet management dashboard
- Microsoft Entra ID authentication (PKCE + Device Code Flow)
- Role-based access control mapped to Entra AD groups
- Policy builder for tool, file, and model restrictions
- Model catalog with encrypted API key storage (AES-256-GCM)
- HMAC-SHA256 signed configuration distribution
- Application security integrations (Checkmarx, Semgrep, Sonatype) via MCP proxy
- White-label branding support
- Pre-configured binary distribution with enrollment tokens
- AI agent TUI with Build, Plan, Explore, and General modes
- Session management with undo/redo, forking, and checkpoints
- 40+ keyboard shortcuts with vim-style navigation
- Command palette with fuzzy search and categories
- Notification center for background events
- Adaptive prompt hints
- Typing indicators and live progress tracking
- MCP (Model Context Protocol) integration
- Project-level extensibility (custom agents, commands, skills, themes, tools)
- Support for 21+ AI providers
- Cross-platform binaries (Linux, macOS, Windows)
- TypeScript SDK (`@ironbark-ai/sdk`)
- Plugin system (`@ironbark-ai/plugin`)
