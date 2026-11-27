# dealcode Plugin for Claude

The **dealcode** plugin pairs the remote dealcode MCP App connector (`https://app.dealcode.ai/mcp/claude`) with workflow skills so Claude works across your dealcode AI Workspace (sales, marketing, recruiting, delivery, and operations on one shared database hosted in Germany), covering shared CRM records, tasks, meetings, campaigns, sequences, funnels, newsletters, social calendars, and your unified inbox.

## What Is Included

- **Remote MCP Connector:** Connects over HTTPS Streamable HTTP to `https://app.dealcode.ai/mcp/claude` using OAuth 2.1 with PKCE (`S256`). Each user signs in with their own dealcode AI Workspace credentials and approves scoped permissions on the consent screen.
- **Interactive MCP App Views:** Displays interactive workspace analytics dashboards, filterable account and pipeline explorers, campaign message previews, and social editorial calendars directly inside Claude.
- **Workflow Skill (`dealcode-workflows`):** Teaches Claude to inspect workspace context before writing, ask concise clarifying questions when business choices are open, confirm category names before imports, and preview campaigns and funnels before publishing or activating them.

## Requirements & Privacy

- Requires an active dealcode AI Workspace (Trial or Enterprise) and a Workspace Owner or Administrator account to authorise the OAuth connection.
- No credentials or API keys are stored in this plugin. All authentication is handled via OAuth 2.1 tokens issued for the user's selected workspace.
- Privacy Policy: https://www.dealcode.ai/en/legal/privacy-policy
- Support: support@dealcode.ai
