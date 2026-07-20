# Agent700: Native API Reference

A consolidated summary of Agent700's API configuration and 80 documented operations, with links to official documentation.

- **Official docs:** https://agent700.readme.io/reference/authentication-4
- **API base URL:** `https://api.agent700.ai/api`

## Authentication

### App Password

Authenticate Agent700 API requests with an Agent700 app password used as a direct bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://agent700.readme.io/reference/authentication-4)

## Endpoints (80 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add MCP Server to Agent](actions/add-mcp-server-to-agent.md) | `POST /agents/:agent_id/mcp/servers` | [docs](https://agent700.readme.io/reference/postagentmcpservers-1) |
| [Add MCP Server with Validation](actions/add-mcp-server-with-validation.md) | `POST /servers/add-with-validation` | [docs](https://agent700.readme.io/reference/postserveraddwithvalidation) |
| [Add User to Organization](actions/add-user-to-organization.md) | `POST /organizations/add_user` | [docs](https://agent700.readme.io/reference/post_api-organizations-add-user) |
| [App Password Login](actions/app-password-login.md) | `POST /auth/app-password-login` | [docs](https://agent700.readme.io/reference/postauthapp-password-login-1) |
| [Bulk Add MCP Servers](actions/bulk-add-mcp-servers.md) | `POST /servers/bulk-add` | [docs](https://agent700.readme.io/reference/getmcpservers-1) |
| [Call MCP Tool for Agent](actions/call-mcp-tool-for-agent.md) | `POST /agents/:agent_id/mcp/tools/call` | [docs](https://agent700.readme.io/reference/postagentmcptoolcall-1) |
| [Chat Completion](actions/chat-completion.md) | `POST /chat` | [docs](https://agent700.readme.io/reference/postchat-1) |
| [Chat Streaming (SSE)](actions/chat-streaming-sse.md) | `POST /stream-chat` | [docs](https://agent700.readme.io/reference/postchat-1) |
| [Complete Email-Based Password Setup](actions/complete-email-based-password-setup.md) | `POST /auth/complete-email-password-setup` | [docs](https://agent700.readme.io/reference/authentication-4) |
| [Complete Password Reset](actions/complete-password-reset.md) | `POST /auth/reset-password` | [docs](https://agent700.readme.io/reference/authentication-4) |
| [Configure Public MCP Servers for Agent](actions/configure-public-mcp-servers-for-agent.md) | `POST /agents/:agent_id/mcp/public-servers` | [docs](https://agent700.readme.io/reference/postagentmcppublicservers-1) |
| [Construct Alignment JSON](actions/construct-alignment-json.md) | `GET /alignment-data/construct-json` | [docs](https://agent700.readme.io/reference/getalignmentdataconstructjson-1) |
| [Construct Alignment JSON by Pattern](actions/construct-alignment-json-by-pattern.md) | `GET /alignment-data/construct-json-by-pattern` | [docs](https://agent700.readme.io/reference/getalignmentdataconstructpattern-1) |
| [Create Agent](actions/create-agent.md) | `POST /agents` | [docs](https://agent700.readme.io/reference/getagents-1) |
| [Create App Password](actions/create-app-password.md) | `POST /auth/app-passwords/create` | [docs](https://agent700.readme.io/reference/postauthapppasswordscreate-1) |
| [Create or Update Alignment Data](actions/create-or-update-alignment-data.md) | `POST /alignment-data` | [docs](https://agent700.readme.io/reference/postalignmentdata-1) |
| [Create Organization](actions/create-organization.md) | `POST /organizations/create` | [docs](https://agent700.readme.io/reference/postorganizationscreate) |
| [Create QA Sheet](actions/create-qa-sheet.md) | `POST /agents/:agent_id/qa-sheets` | [docs](https://agent700.readme.io/reference/postagentqasheets-1) |
| [Create Rating](actions/create-rating.md) | `POST /ratings` | [docs](https://agent700.readme.io/reference/get_api-ratings-export) |
| [Create Workflow](actions/create-workflow.md) | `POST /workflows` | [docs](https://agent700.readme.io/reference/postworkflows-1) |
| [Delete Agent](actions/delete-agent.md) | `DELETE /agents/:agent_id` | [docs](https://agent700.readme.io/reference/delete_api-agents-agent-id) |
| [Delete Alignment Data](actions/delete-alignment-data.md) | `DELETE /alignment-data/by-key/:key` | [docs](https://agent700.readme.io/reference/getalignmentdata-1) |
| [Delete App Password](actions/delete-app-password.md) | `DELETE /auth/app-passwords/:app_password_id` | [docs](https://agent700.readme.io/reference/deleteauthapppasswordbyid-1) |
| [Delete MCP Server](actions/delete-mcp-server.md) | `DELETE /mcp/servers/:server_id` | [docs](https://agent700.readme.io/reference/delete_api-mcp-servers-server-id) |
| [Delete QA Sheet](actions/delete-qa-sheet.md) | `DELETE /agents/:agent_id/qa-sheets/:qa_sheet_id` | [docs](https://agent700.readme.io/reference/postagentqasheets-1) |
| [Discover MCP Server Capabilities](actions/discover-mcp-server-capabilities.md) | `POST /servers/discover` | [docs](https://agent700.readme.io/reference/postserverdiscover-1) |
| [Email/Password Login](actions/email-password-login.md) | `POST /auth/login` | [docs](https://agent700.readme.io/reference/authentication-4) |
| [Email/Password Signup](actions/email-password-signup.md) | `POST /auth/signup` | [docs](https://agent700.readme.io/reference/postauthsignup-1) |
| [Export MCP Server Configs](actions/export-mcp-server-configs.md) | `GET /servers/export` | [docs](https://agent700.readme.io/reference/getserverexport-1) |
| [Export Ratings as CSV](actions/export-ratings-as-csv.md) | `GET /ratings-export` | [docs](https://agent700.readme.io/reference/get_api-ratings-export) |
| [Fetch URL Metadata](actions/fetch-url-metadata.md) | `GET /chat/fetch-url-metadata` | [docs](https://agent700.readme.io/reference/postchat-1) |
| [Get Agent by ID](actions/get-agent-details.md) | `GET /agents/:agent_id` | [docs](https://agent700.readme.io/reference/get_api-agents-agent-id) |
| [Get Agent Sharing Info](actions/get-agent-sharing-info.md) | `GET /agents/:agent_id/sharing` | [docs](https://agent700.readme.io/reference/getagentsharinginfo-1) |
| [Get Alignment Data by Key](actions/get-alignment-data-by-key.md) | `GET /alignment-data/by-key/:key` | [docs](https://agent700.readme.io/reference/getalignmentdatabykey-1) |
| [Get MCP Tool Definitions for Agent](actions/get-mcp-tool-definitions-for-agent.md) | `GET /agents/:agent_id/mcp/tools` | [docs](https://agent700.readme.io/reference/getagentmcptools-1) |
| [Get Organization Billing Logs](actions/get-organization-billing-logs.md) | `GET /billing/logs/organization` | [docs](https://agent700.readme.io/reference/getagents-1) |
| [Get QA Sheet](actions/get-qa-sheet.md) | `GET /agents/:agent_id/qa-sheets/:qa_sheet_id` | [docs](https://agent700.readme.io/reference/postagentqasheets-1) |
| [Get User Billing Logs](actions/get-user-billing-logs.md) | `GET /billing/logs/user` | [docs](https://agent700.readme.io/reference/getagents-1) |
| [Get Workflow by ID](actions/get-workflow-by-id.md) | `GET /workflows/:workflow_id` | [docs](https://agent700.readme.io/reference/getworkflowbyid-1) |
| [Get Workflow Revision by ID](actions/get-workflow-revision-by-id.md) | `GET /workflows/:workflow_id/revisions/:revision_id` | [docs](https://agent700.readme.io/reference/getworkflowrevisionbyid-1) |
| [Google OAuth Callback (Token-Based)](actions/google-o-auth-callback-token-based.md) | `POST /auth/google/callback` | [docs](https://agent700.readme.io/reference/authentication-4) |
| [JWT Heartbeat](actions/j-wt-heartbeat.md) | `POST /auth/heartbeat` | [docs](https://agent700.readme.io/reference/postauthheartbeat-1) |
| [List Agents](actions/list-agents.md) | `GET /agents` | [docs](https://agent700.readme.io/reference/getagents-1) |
| [List Alignment Data](actions/list-alignment-data.md) | `GET /alignment-data` | [docs](https://agent700.readme.io/reference/getalignmentdata-1) |
| [List Alignment Data Key-Value Pairs by Pattern](actions/list-alignment-data-key-value-pairs-by-pattern.md) | `GET /alignment-data/list-kv-by-pattern` | [docs](https://agent700.readme.io/reference/getalignmentdatakvpattern-1) |
| [List App Passwords](actions/list-app-passwords.md) | `GET /auth/app-passwords` | [docs](https://agent700.readme.io/reference/getauthapppasswords-1) |
| [List MCP Servers](actions/list-mcp-servers.md) | `GET /mcp/servers` | [docs](https://agent700.readme.io/reference/getmcpservers-1) |
| [List MCP Servers for Agent](actions/list-mcp-servers-for-agent.md) | `GET /agents/:agent_id/mcp/servers` | [docs](https://agent700.readme.io/reference/getagentmcpservers-1) |
| [List My Organizations](actions/list-my-organizations.md) | `GET /organizations/my` | [docs](https://agent700.readme.io/reference) |
| [List Organization Members](actions/list-organization-members.md) | `GET /organizations/members` | [docs](https://agent700.readme.io/reference) |
| [List QA Sheets for Agent](actions/list-qa-sheets-for-agent.md) | `GET /agents/:agent_id/qa-sheets` | [docs](https://agent700.readme.io/reference/postagentqasheets-1) |
| [List Ratings for Agent](actions/list-ratings-for-agent.md) | `GET /ratings/agent/:agent_id` | [docs](https://agent700.readme.io/reference/get_api-ratings-export) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://agent700.readme.io/reference/getworkflows-1) |
| [Logout](actions/logout.md) | `POST /auth/logout` | [docs](https://agent700.readme.io/reference/authentication-4) |
| [MCP Health](actions/m-cp-health.md) | `GET /mcp/health` | [docs](https://agent700.readme.io/reference/get_api-mcp-health) |
| [MCP Health for Agent](actions/m-cp-health-for-agent.md) | `GET /agents/:agent_id/mcp/health` | [docs](https://agent700.readme.io/reference/getagentmcphealth-1) |
| [Parse Document](actions/parse-document.md) | `POST /helpers/parse-document` | [docs](https://agent700.readme.io/reference/posthelpersparsedocument-1) |
| [Read MCP Resource](actions/read-mcp-resource.md) | `POST /mcp/resources/read` | [docs](https://agent700.readme.io/reference/post_api-mcp-resources-read) |
| [Read MCP Resource for Agent](actions/read-mcp-resource-for-agent.md) | `POST /agents/:agent_id/mcp/resources/read` | [docs](https://agent700.readme.io/reference/post_api-mcp-resources-read) |
| [Refresh Access Token](actions/refresh-access-token.md) | `POST /auth/refresh` | [docs](https://agent700.readme.io/reference/authentication-4) |
| [Register MCP Server](actions/register-mcp-server.md) | `POST /mcp/servers` | [docs](https://agent700.readme.io/reference/postmcpservers-1) |
| [Remove MCP Server from Agent](actions/remove-mcp-server-from-agent.md) | `DELETE /agents/:agent_id/mcp/servers/:server_id` | [docs](https://agent700.readme.io/reference/deleteagentmcpserverbyid-1) |
| [Remove User from Organization](actions/remove-user-from-organization.md) | `DELETE /organizations/remove_user` | [docs](https://agent700.readme.io/reference) |
| [Request Password Reset](actions/request-password-reset.md) | `POST /auth/request-password-reset` | [docs](https://agent700.readme.io/reference/authentication-4) |
| [Reset Password (Authenticated)](actions/reset-password-authenticated.md) | `POST /auth/reset-password-authenticated` | [docs](https://agent700.readme.io/reference/authentication-4) |
| [Restart MCP Server for Agent](actions/restart-mcp-server-for-agent.md) | `POST /agents/:agent_id/mcp/servers/:server_name/restart` | [docs](https://agent700.readme.io/reference/postagentmcpserverrestart-1) |
| [SSE Streaming Health](actions/s-se-streaming-health.md) | `GET /chat/streaming/health` | [docs](https://agent700.readme.io/reference/getstreaminghealth) |
| [Socket.IO WebSocket Realtime API](actions/socket-io-web-socket-realtime-api.md) | `GET /realtime` | [docs](https://agent700.readme.io/reference) |
| [Start Google OAuth Login](actions/start-google-o-auth-login.md) | `GET /auth/google` | [docs](https://agent700.readme.io/reference/getauthgoogle-1) |
| [Streaming Statistics](actions/streaming-statistics.md) | `GET /chat/streaming/stats` | [docs](https://agent700.readme.io/reference/getstreamingstats) |
| [Test MCP Server Connection](actions/test-mcp-server-connection.md) | `POST /servers/:server_name/test-connection` | [docs](https://agent700.readme.io/reference/postservertestconnection-1) |
| [Toggle MCP Server Enabled State](actions/toggle-mcp-server-enabled-state.md) | `POST /mcp/servers/:server_name/toggle` | [docs](https://agent700.readme.io/reference/getmcpservers-1) |
| [Toggle MCP Server Enabled State for Agent](actions/toggle-mcp-server-enabled-state-for-agent.md) | `POST /agents/:agent_id/mcp/servers/:server_name/toggle` | [docs](https://agent700.readme.io/reference/postagentmcpservertoggle-1) |
| [Duplicate Agent](actions/update-agent.md) | `PUT /agents/:agent_id` | [docs](https://agent700.readme.io/reference/putagentbyid-1) |
| [Update Agent Sharing](actions/update-agent-sharing.md) | `POST /agents/:agent_id/share` | [docs](https://agent700.readme.io/reference/getagents-1) |
| [Update or Rename Alignment Data](actions/update-or-rename-alignment-data.md) | `PUT /alignment-data/by-key/:key` | [docs](https://agent700.readme.io/reference/put_api-alignment-data-by-key-key) |
| [Update QA Sheet (New Revision)](actions/update-qa-sheet-new-revision.md) | `PUT /agents/:agent_id/qa-sheets/:qa_sheet_id` | [docs](https://agent700.readme.io/reference/postagentqasheets-1) |
| [Update Rating](actions/update-rating.md) | `PUT /ratings/:rating_id` | [docs](https://agent700.readme.io/reference/get_api-ratings-export) |
| [Update Workflow (New Revision)](actions/update-workflow-new-revision.md) | `PUT /workflows/:workflow_id` | [docs](https://agent700.readme.io/reference/putworkflowbyid-1) |
| [Validate MCP Server URL](actions/validate-mcp-server-url.md) | `POST /servers/validate` | [docs](https://agent700.readme.io/reference/postservervalidate) |
