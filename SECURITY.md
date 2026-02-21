# Security

## Threat Model

### Overview

Ironbark is an enterprise AI agent platform that runs within your organisation's infrastructure. It provides an agent system with access to tools including shell execution, file operations, and web access, all governed by centrally managed policies and RBAC.

### Enterprise Security Controls

Ironbark extends the base agent with enterprise security features:

- **Entra ID Authentication**: All access requires Microsoft Entra ID (Azure AD) authentication via PKCE or Device Code Flow
- **Role-Based Access Control (RBAC)**: Centrally managed roles with fine-grained tool and file permissions
- **Policy Engine**: Configurable policies to block destructive commands, protect sensitive files, and restrict tool usage
- **Config Lockdown**: Managed configuration prevents end users from overriding security controls
- **HMAC Config Signing**: Configuration integrity verification prevents tampering
- **Audit Trail**: Agent actions are logged for compliance and security review
- **LLM Lockdown**: Only admin-provisioned AI models and API keys are available; no user-supplied credentials

### Agent Permissions

The permission system is enforced by the enterprise policy engine. Administrators configure tool permissions, file access patterns, and model access through the Admin Console. The agent respects these controls at runtime.

### Server Mode

When server mode is enabled, it is restricted to loopback-only (`127.0.0.1`) in enterprise lockdown mode. mDNS discovery is disabled.

### Out of Scope

| Category                        | Rationale                                                                  |
| ------------------------------- | -------------------------------------------------------------------------- |
| **LLM provider data handling**  | Data sent to your configured LLM provider is governed by their policies    |
| **MCP server behaviour**        | Admin-configured MCP servers operate under their own trust boundaries      |
| **Infrastructure security**     | Host OS, network, and container security is your organisation's responsibility |

---

# Reporting Security Issues

We appreciate your efforts to responsibly disclose your findings, and will make every effort to acknowledge your contributions.

To report a security issue, please email **security@vindcom.com.au** with:

- A description of the vulnerability
- Steps to reproduce
- Potential impact assessment

We will acknowledge receipt within 3 business days and provide a timeline for remediation.

## Responsible Disclosure

Please do not publicly disclose the vulnerability until we have had a reasonable opportunity to address it. We commit to keeping you informed of progress toward a fix.
