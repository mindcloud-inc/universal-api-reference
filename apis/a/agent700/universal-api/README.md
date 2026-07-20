# <img src="https://images.mindcloud.co/apps/icons/agent700_1775756832048.png" alt="Agent700 logo" width="28" height="28"> Agent700: Universal API

Agent700 is an AgentOS platform for building, deploying, automating, and scaling secure private AI agents across workflows, QA, alignment data, and MCP operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agent700/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 80
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.agent700.ai
- **Vendor API docs:** https://agent700.readme.io/reference/authentication-4

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agents](actions/list-agents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agent700/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (80)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST |  |
| [Delete Agent](actions/delete-agent.md) | DELETE |  |
| [Get Agent by ID](actions/get-agent-details.md) | GET |  |
| [List Agents](actions/list-agents.md) | GET |  |
| [Duplicate Agent](actions/update-agent.md) | PUT |  |

### Agent Mcp Health

| Action | Method | Description |
| --- | --- | --- |
| [MCP Health for Agent](actions/m-cp-health-for-agent.md) | GET |  |

### Agent Mcp Resource

| Action | Method | Description |
| --- | --- | --- |
| [Read MCP Resource for Agent](actions/read-mcp-resource-for-agent.md) | GET |  |

### Agent Mcp Server

| Action | Method | Description |
| --- | --- | --- |
| [Add MCP Server to Agent](actions/add-mcp-server-to-agent.md) | POST |  |
| [Configure Public MCP Servers for Agent](actions/configure-public-mcp-servers-for-agent.md) | PUT |  |
| [List MCP Servers for Agent](actions/list-mcp-servers-for-agent.md) | GET |  |
| [Remove MCP Server from Agent](actions/remove-mcp-server-from-agent.md) | DELETE |  |
| [Restart MCP Server for Agent](actions/restart-mcp-server-for-agent.md) | PUT |  |
| [Toggle MCP Server Enabled State for Agent](actions/toggle-mcp-server-enabled-state-for-agent.md) | PUT |  |

### Agent Mcp Tool Call

| Action | Method | Description |
| --- | --- | --- |
| [Call MCP Tool for Agent](actions/call-mcp-tool-for-agent.md) | POST |  |

### Agent Mcp Tool Definition

| Action | Method | Description |
| --- | --- | --- |
| [Get MCP Tool Definitions for Agent](actions/get-mcp-tool-definitions-for-agent.md) | GET |  |

### Agent Sharing

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Sharing Info](actions/get-agent-sharing-info.md) | GET |  |
| [Update Agent Sharing](actions/update-agent-sharing.md) | POST |  |

### Alignment Data

| Action | Method | Description |
| --- | --- | --- |
| [Construct Alignment JSON](actions/construct-alignment-json.md) | GET |  |
| [Construct Alignment JSON by Pattern](actions/construct-alignment-json-by-pattern.md) | GET |  |
| [Create or Update Alignment Data](actions/create-or-update-alignment-data.md) | PUT |  |
| [Delete Alignment Data](actions/delete-alignment-data.md) | DELETE |  |
| [Get Alignment Data by Key](actions/get-alignment-data-by-key.md) | GET |  |
| [List Alignment Data](actions/list-alignment-data.md) | GET |  |
| [List Alignment Data Key-Value Pairs by Pattern](actions/list-alignment-data-key-value-pairs-by-pattern.md) | GET |  |
| [Update or Rename Alignment Data](actions/update-or-rename-alignment-data.md) | PUT |  |

### App Password

| Action | Method | Description |
| --- | --- | --- |
| [App Password Login](actions/app-password-login.md) | POST |  |
| [Create App Password](actions/create-app-password.md) | POST |  |
| [Delete App Password](actions/delete-app-password.md) | DELETE |  |
| [List App Passwords](actions/list-app-passwords.md) | GET |  |

### Billing Log

| Action | Method | Description |
| --- | --- | --- |
| [Get User Billing Logs](actions/get-user-billing-logs.md) | GET |  |

### Chat Response

| Action | Method | Description |
| --- | --- | --- |
| [Chat Completion](actions/chat-completion.md) | GET |  |
| [Chat Streaming (SSE)](actions/chat-streaming-sse.md) | GET |  |

### Document Parse

| Action | Method | Description |
| --- | --- | --- |
| [Parse Document](actions/parse-document.md) | GET |  |

### Mcp Capability

| Action | Method | Description |
| --- | --- | --- |
| [Discover MCP Server Capabilities](actions/discover-mcp-server-capabilities.md) | GET |  |

### Mcp Health

| Action | Method | Description |
| --- | --- | --- |
| [MCP Health](actions/m-cp-health.md) | GET |  |

### Mcp Resource

| Action | Method | Description |
| --- | --- | --- |
| [Read MCP Resource](actions/read-mcp-resource.md) | GET |  |

### Mcp Server

| Action | Method | Description |
| --- | --- | --- |
| [Add MCP Server with Validation](actions/add-mcp-server-with-validation.md) | POST |  |
| [Bulk Add MCP Servers](actions/bulk-add-mcp-servers.md) | POST |  |
| [Delete MCP Server](actions/delete-mcp-server.md) | DELETE |  |
| [List MCP Servers](actions/list-mcp-servers.md) | GET |  |
| [Register MCP Server](actions/register-mcp-server.md) | POST |  |
| [Test MCP Server Connection](actions/test-mcp-server-connection.md) | POST |  |
| [Toggle MCP Server Enabled State](actions/toggle-mcp-server-enabled-state.md) | PUT |  |

### Mcp Server Export

| Action | Method | Description |
| --- | --- | --- |
| [Export MCP Server Configs](actions/export-mcp-server-configs.md) | GET |  |

### Mcp Server Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate MCP Server URL](actions/validate-mcp-server-url.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST |  |
| [Get Organization Billing Logs](actions/get-organization-billing-logs.md) | GET |  |
| [List My Organizations](actions/list-my-organizations.md) | GET |  |

### Organization Membership

| Action | Method | Description |
| --- | --- | --- |
| [Add User to Organization](actions/add-user-to-organization.md) | POST |  |
| [List Organization Members](actions/list-organization-members.md) | GET |  |
| [Remove User from Organization](actions/remove-user-from-organization.md) | DELETE |  |

### Password Reset

| Action | Method | Description |
| --- | --- | --- |
| [Complete Password Reset](actions/complete-password-reset.md) | PUT |  |
| [Request Password Reset](actions/request-password-reset.md) | PUT |  |

### Qa Sheet

| Action | Method | Description |
| --- | --- | --- |
| [Create QA Sheet](actions/create-qa-sheet.md) | POST |  |
| [Delete QA Sheet](actions/delete-qa-sheet.md) | DELETE |  |
| [Get QA Sheet](actions/get-qa-sheet.md) | GET |  |
| [List QA Sheets for Agent](actions/list-qa-sheets-for-agent.md) | GET |  |
| [Update QA Sheet (New Revision)](actions/update-qa-sheet-new-revision.md) | PUT |  |

### Rating

| Action | Method | Description |
| --- | --- | --- |
| [Create Rating](actions/create-rating.md) | POST |  |
| [List Ratings for Agent](actions/list-ratings-for-agent.md) | GET |  |
| [Update Rating](actions/update-rating.md) | PUT |  |

### Rating Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Ratings as CSV](actions/export-ratings-as-csv.md) | GET |  |

### Realtime Session

| Action | Method | Description |
| --- | --- | --- |
| [Socket.IO WebSocket Realtime API](actions/socket-io-web-socket-realtime-api.md) | GET |  |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Complete Email-Based Password Setup](actions/complete-email-based-password-setup.md) | PUT |  |
| [Email/Password Signup](actions/email-password-signup.md) | POST |  |
| [Reset Password (Authenticated)](actions/reset-password-authenticated.md) | PUT |  |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Email/Password Login](actions/email-password-login.md) | POST |  |
| [Google OAuth Callback (Token-Based)](actions/google-o-auth-callback-token-based.md) | POST |  |
| [JWT Heartbeat](actions/j-wt-heartbeat.md) | GET |  |
| [Logout](actions/logout.md) | DELETE |  |
| [Refresh Access Token](actions/refresh-access-token.md) | PUT |  |
| [Start Google OAuth Login](actions/start-google-o-auth-login.md) | GET |  |

### Streaming Health

| Action | Method | Description |
| --- | --- | --- |
| [SSE Streaming Health](actions/s-se-streaming-health.md) | GET |  |

### Streaming Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Streaming Statistics](actions/streaming-statistics.md) | GET |  |

### Url Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Fetch URL Metadata](actions/fetch-url-metadata.md) | GET |  |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST |  |
| [Get Workflow by ID](actions/get-workflow-by-id.md) | GET |  |
| [List Workflows](actions/list-workflows.md) | GET |  |
| [Update Workflow (New Revision)](actions/update-workflow-new-revision.md) | PUT |  |

### Workflow Revision

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Revision by ID](actions/get-workflow-revision-by-id.md) | GET |  |

