# Port API AI: Native API Reference

A consolidated summary of Port API AI's API configuration and 147 documented operations, with links to official documentation.

- **Official docs:** https://docs.port.io/api-reference/port-api/
- **API base URL:** `https://api.port.io/v1`

## Authentication

### Port Access Token

Stores a Port runtime access token obtained from the Port client credentials bootstrap flow.

### Credentials

- **Access Token:** `accessToken` · optional · Port runtime access token returned by POST /v1/auth/access_token.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://docs.port.io/api-reference/port-api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (147 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Action Run Log](actions/add-action-run-log.md) | `POST /actions/runs/:run_id/logs` | [docs](https://docs.port.io/api-reference/add-a-log-to-an-action-run) |
| [Aggregate Entities](actions/aggregate-entities.md) | `POST /entities/aggregate` | [docs](https://docs.port.io/api-reference/aggregate-entities) |
| [Aggregate Entities Over Time](actions/aggregate-entities-over-time.md) | `POST /entities/aggregate-over-time` | [docs](https://docs.port.io/api-reference/aggregate-entities-over-time) |
| [Approve Action Run](actions/approve-action-run.md) | `PATCH /actions/runs/:run_id/approval` | [docs](https://docs.port.io/api-reference/approve-an-action-run) |
| [Call MCP Server Tool](actions/call-mcp-server-tool.md) | `POST /mcp/servers/:server_id/tools/:tool_name/call` | [docs](https://docs.port.io/api-reference/call-mcp-server-tool) |
| [Cancel Migration](actions/cancel-migration.md) | `POST /migrations/:migration_id/cancel` | [docs](https://docs.port.io/api-reference/cancel-a-migration) |
| [Create Action Automation](actions/create-action-automation.md) | `POST /actions` | [docs](https://docs.port.io/api-reference/create-an-action-automation) |
| [Create Auto Discovery Invocation](actions/create-auto-discovery-invocation.md) | `POST /ai/entities-auto-discovery` | [docs](https://docs.port.io/api-reference/create-an-auto-discovery-invocation) |
| [Create Blueprint](actions/create-blueprint.md) | `POST /blueprints` | [docs](https://docs.port.io/api-reference/create-a-blueprint) |
| [Create Credential Set](actions/create-credential-set.md) | `POST /apps` | [docs](https://docs.port.io/api-reference/create-credentials) |
| [Create Entity](actions/create-entity.md) | `POST /blueprints/:blueprint_identifier/entities` | [docs](https://docs.port.io/api-reference/create-an-entity) |
| [Create LLM Provider](actions/create-llm-provider.md) | `POST /llm-providers` | [docs](https://docs.port.io/api-reference/create-or-connect-an-llm-provider) |
| [Create Migration](actions/create-migration.md) | `POST /migrations` | [docs](https://docs.port.io/api-reference/create-a-migration) |
| [Create Multiple Entities](actions/create-multiple-entities.md) | `POST /blueprints/:blueprint_identifier/entities/bulk` | [docs](https://docs.port.io/api-reference/create-multiple-entities) |
| [Create Organization Secret](actions/create-organization-secret.md) | `POST /organization/secrets` | [docs](https://docs.port.io/api-reference/create-an-organization-secret) |
| [Create Scorecard](actions/create-scorecard.md) | `POST /blueprints/:blueprint_identifier/scorecards` | [docs](https://docs.port.io/api-reference/create-a-scorecard) |
| [Create Team](actions/create-team.md) | `POST /teams` | [docs](https://docs.port.io/api-reference/create-a-team) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.port.io/api-reference/create-a-webhook) |
| [Create Workflow](actions/create-workflow.md) | `POST /workflows` | [docs](https://docs.port.io/api-reference/create-a-workflow) |
| [Create Workflow Node Permissions](actions/create-workflow-node-permissions.md) | `POST /workflows/:workflow_identifier/nodes/:node_identifier/permissions` | [docs](https://docs.port.io/api-reference/create-workflow-node-permissions) |
| [Delete Action Automation](actions/delete-action-automation.md) | `DELETE /actions/:action_identifier` | [docs](https://docs.port.io/api-reference/delete-an-action-automation) |
| [Delete AI Invocation Feedback](actions/delete-ai-invocation-feedback.md) | `DELETE /ai/invoke/:invocation_identifier/feedback` | [docs](https://docs.port.io/api-reference/delete-ai-invocation-feedback) |
| [Delete Blueprint](actions/delete-blueprint.md) | `DELETE /blueprints/:identifier` | [docs](https://docs.port.io/api-reference/delete-a-blueprint) |
| [Delete Credential Set](actions/delete-credential-set.md) | `DELETE /apps/:id` | [docs](https://docs.port.io/api-reference/delete-credentials) |
| [Delete Entity](actions/delete-entity.md) | `DELETE /blueprints/:blueprint_identifier/entities/:entity_identifier` | [docs](https://docs.port.io/api-reference/delete-an-entity) |
| [Delete Integration](actions/delete-integration.md) | `DELETE /integration/:identifier` | [docs](https://docs.port.io/api-reference/delete-an-integration) |
| [Delete LLM Provider](actions/delete-llm-provider.md) | `DELETE /llm-providers/:provider` | [docs](https://docs.port.io/api-reference/delete-a-specific-provider-configuration) |
| [Delete Memory Records](actions/delete-memory-records.md) | `DELETE /memory` | [docs](https://docs.port.io/api-reference/delete-user-memory-records) |
| [Delete Memory Users](actions/delete-memory-users.md) | `DELETE /memory/users` | [docs](https://docs.port.io/api-reference/delete-users-memory-records/) |
| [Delete Multiple Entities](actions/delete-multiple-entities.md) | `POST /blueprints/:blueprint_identifier/bulk/entities/delete` | [docs](https://docs.port.io/api-reference/delete-multiple-entities) |
| [Delete Organization Secret](actions/delete-organization-secret.md) | `DELETE /organization/secrets/:secret_name` | [docs](https://docs.port.io/api-reference/delete-an-organization-secret) |
| [Delete Page](actions/delete-page.md) | `DELETE /pages/:identifier` | [docs](https://docs.port.io/api-reference/delete-a-page) |
| [Delete Page Widget](actions/delete-page-widget.md) | `DELETE /pages/:page_identifier/widgets/:widget_id` | [docs](https://docs.port.io/api-reference/delete-a-widget/) |
| [Delete Plugin](actions/delete-plugin.md) | `DELETE /plugins/:identifier` | [docs](https://docs.port.io/api-reference/delete-a-plugin-by-identifier) |
| [Delete Scorecard](actions/delete-scorecard.md) | `DELETE /blueprints/:blueprint_identifier/scorecards/:scorecard_identifier` | [docs](https://docs.port.io/api-reference/delete-a-scorecard) |
| [Delete Team](actions/delete-team.md) | `DELETE /teams/:name` | [docs](https://docs.port.io/api-reference/delete-a-team) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:user_email` | [docs](https://docs.port.io/api-reference/delete-a-user) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:identifier` | [docs](https://docs.port.io/api-reference/delete-a-webhook) |
| [Delete Workflow](actions/delete-workflow.md) | `DELETE /workflows/:workflow_identifier` | [docs](https://docs.port.io/api-reference/delete-a-workflow) |
| [Delete Workflow Node Permissions](actions/delete-workflow-node-permissions.md) | `DELETE /workflows/:workflow_identifier/nodes/:node_identifier/permissions` | [docs](https://docs.port.io/api-reference/delete-a-workflows-node-permissions) |
| [Disconnect MCP User Server](actions/disconnect-mcp-user-server.md) | `DELETE /mcp/user/servers/:server_id` | [docs](https://docs.port.io/api-reference/disconnect-mcp-server) |
| [Finalize Plugin Upload](actions/finalize-plugin-upload.md) | `POST /plugins/finalize-upload` | [docs](https://docs.port.io/api-reference/finalize-a-plugin-upload) |
| [Get Action Automation](actions/get-action-automation.md) | `GET /actions/:action_identifier` | [docs](https://docs.port.io/api-reference/get-an-action-automation) |
| [Get Action Permissions](actions/get-action-permissions.md) | `GET /actions/:action_identifier/permissions` | [docs](https://docs.port.io/api-reference/get-an-actions-permissions) |
| [Get Action Run](actions/get-action-run.md) | `GET /actions/runs/:run_id` | [docs](https://docs.port.io/api-reference/get-an-action-runs-details) |
| [Get Action Run Logs](actions/get-action-run-logs.md) | `GET /actions/runs/:run_id/logs` | [docs](https://docs.port.io/api-reference/get-an-actions-run-logs) |
| [Get AI Invocation](actions/get-ai-invocation.md) | `GET /ai/invoke/:invocation_identifier` | [docs](https://docs.port.io/api-reference/get-an-invocations-result) |
| [Get AI Invocation Quota](actions/get-ai-invocation-quota.md) | `GET /quota/ai-invocations` | [docs](https://docs.port.io/api-reference/get-monthly-ai-invocations-quota-usage) |
| [Get Audit Logs](actions/get-audit-logs.md) | `GET /audit-log` | [docs](https://docs.port.io/api-reference/get-audit-logs) |
| [Get Auto Discovery Suggestions](actions/get-auto-discovery-suggestions.md) | `GET /ai/entities-auto-discovery/:invocation_id/suggestions` | [docs](https://docs.port.io/api-reference/get-auto-discovery-invocation-suggestions) |
| [Get Blueprint](actions/get-blueprint.md) | `GET /blueprints/:identifier` | [docs](https://docs.port.io/api-reference/get-a-blueprint) |
| [Get Blueprint Entity Count](actions/get-blueprint-entity-count.md) | `GET /blueprints/:blueprint_identifier/entities-count` | [docs](https://docs.port.io/api-reference/get-a-blueprints-entity-count) |
| [Get Blueprint Permissions](actions/get-blueprint-permissions.md) | `GET /blueprints/:blueprint_identifier/permissions` | [docs](https://docs.port.io/api-reference/get-a-blueprints-permissions) |
| [Get Default LLM Provider](actions/get-default-llm-provider.md) | `GET /llm-providers/defaults` | [docs](https://docs.port.io/api-reference/get-default-llm-provider-and-model) |
| [Get Entity](actions/get-entity.md) | `GET /blueprints/:blueprint_identifier/entities/:entity_identifier` | [docs](https://docs.port.io/api-reference/get-an-entity) |
| [Get Entity Properties History](actions/get-entity-properties-history.md) | `POST /entities/properties-history` | [docs](https://docs.port.io/api-reference/fetch-the-history-of-an-entitys-properties) |
| [Get Integration](actions/get-integration.md) | `GET /integration/:identifier` | [docs](https://docs.port.io/api-reference/get-an-integration) |
| [Get Integration Logs](actions/get-integration-logs.md) | `GET /integration/:identifier/logs` | [docs](https://docs.port.io/api-reference/get-an-integrations-event-logs) |
| [Get Integration Metadata](actions/get-integration-metadata.md) | `GET /integration/metadata` | [docs](https://www.docs.port.io/api-reference/get-all-integrations-meta-data-member-view) |
| [Get Integration Sync Metadata](actions/get-integration-sync-metadata.md) | `GET /integration/:integrationInternalId/syncsMetadata` | [docs](https://docs.port.io/api-reference/get-an-integrations-sync-metadata) |
| [Get Integration Sync Metrics](actions/get-integration-sync-metrics.md) | `GET /integration/:integrationInternalId/syncMetrics` | [docs](https://docs.port.io/api-reference/get-an-integrations-metrics-and-sync-status) |
| [Get Latest Auto Discovery Invocation](actions/get-latest-auto-discovery-invocation.md) | `GET /ai/entities-auto-discovery/blueprint/:blueprint_identifier/latest` | [docs](https://docs.port.io/api-reference/get-latest-auto-discovery-invocation-for-a-blueprint) |
| [Get LLM Provider](actions/get-llm-provider.md) | `GET /llm-providers/:provider` | [docs](https://docs.port.io/api-reference/get-a-specific-provider-configuration) |
| [Get MCP User Server](actions/get-mcp-user-server.md) | `GET /mcp/user/servers/:server_id` | [docs](https://docs.port.io/api-reference/get-mcp-server-by-id) |
| [Get MCP OAuth2 Session Token](actions/get-mcpo-auth2-session-token.md) | `GET /mcp/oauth2/servers/:server_id/session-token` | [docs](https://docs.port.io/api-reference/get-mcp-oauth2-session-token) |
| [Get Memory Settings](actions/get-memory-settings.md) | `GET /memory/settings` | [docs](https://docs.port.io/api-reference/get-memory-settings) |
| [Get Migration](actions/get-migration.md) | `GET /migrations/:migration_id` | [docs](https://docs.port.io/api-reference/get-a-migration) |
| [Get Organization](actions/get-organization.md) | `GET /organization` | [docs](https://docs.port.io/api-reference/get-organization-details) |
| [Get Organization Secret](actions/get-organization-secret.md) | `GET /organization/secrets/:secret_name` | [docs](https://docs.port.io/api-reference/get-an-organization-secrets-metadata) |
| [Get Page](actions/get-page.md) | `GET /pages/:identifier` | [docs](https://docs.port.io/api-reference/get-a-page) |
| [Get Page Permissions](actions/get-page-permissions.md) | `GET /pages/:page_identifier/permissions` | [docs](https://docs.port.io/api-reference/get-a-pages-permissions) |
| [Get Plugin](actions/get-plugin.md) | `GET /plugins/:identifier` | [docs](https://docs.port.io/api-reference/get-a-plugin-by-identifier) |
| [Get Plugin Update Upload URL](actions/get-plugin-update-upload-url.md) | `PUT /plugins/:identifier/upload-url` | [docs](https://docs.port.io/api-reference/get-a-presigned-url-for-plugin-updates) |
| [Get Plugin Upload URL](actions/get-plugin-upload-url.md) | `POST /plugins/upload-url` | [docs](https://docs.port.io/api-reference/get-a-presigned-url-for-uploading-a-plugin) |
| [Get Prompt](actions/get-prompt.md) | `POST /mcp/prompts/:prompt_name` | [docs](https://docs.port.io/api-reference/get-prompt-by-name) |
| [Get Scorecard](actions/get-scorecard.md) | `GET /blueprints/:blueprint_identifier/scorecards/:scorecard_identifier` | [docs](https://docs.port.io/api-reference/get-a-scorecard) |
| [Get Team](actions/get-team.md) | `GET /teams/:name` | [docs](https://docs.port.io/api-reference/get-a-team) |
| [Get User](actions/get-user.md) | `GET /users/:user_email` | [docs](https://docs.port.io/api-reference/get-a-user) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:identifier` | [docs](https://docs.port.io/api-reference/get-a-webhook) |
| [Get Webhook Metadata](actions/get-webhook-metadata.md) | `GET /webhooks/metadata` | [docs](https://docs.port.io/api-reference/get-all-webhooks-meta-data-member-view) |
| [Get Workflow](actions/get-workflow.md) | `GET /workflows/:workflow_identifier` | [docs](https://docs.port.io/api-reference/get-a-workflow) |
| [Get Workflow Node](actions/get-workflow-node.md) | `GET /workflows/:workflow_identifier/nodes/:node_identifier` | [docs](https://docs.port.io/api-reference/get-a-workflows-node) |
| [Get Workflow Node Permissions](actions/get-workflow-node-permissions.md) | `GET /workflows/:workflow_identifier/nodes/:node_identifier/permissions` | [docs](https://docs.port.io/api-reference/get-a-workflows-node-permissions) |
| [Get Workflow Run](actions/get-workflow-run.md) | `GET /workflows/runs/:identifier` | [docs](https://docs.port.io/api-reference/get-a-workflow-run-by-identifier) |
| [Handle MCP OAuth2 Callback](actions/handle-mcpo-auth2-callback.md) | `GET /mcp/oauth2/callback` | [docs](https://docs.port.io/api-reference/mcp-oauth2-callback) |
| [Invite User](actions/invite-user.md) | `POST /users/invite` | [docs](https://docs.port.io/api-reference/invite-a-user-to-your-organization) |
| [Invoke AI](actions/invoke-ai.md) | `POST /ai/invoke` | [docs](https://docs.port.io/api-reference/general-purpose-ai-interactions) |
| [List Action Automations](actions/list-action-automations.md) | `GET /actions` | [docs](https://docs.port.io/api-reference/get-actions-automations) |
| [List Action Run Approvers](actions/list-action-run-approvers.md) | `GET /actions/runs/:run_id/approvers` | [docs](https://docs.port.io/api-reference/get-an-action-runs-approvers) |
| [List Action Runs](actions/list-action-runs.md) | `GET /actions/runs` | [docs](https://docs.port.io/api-reference/get-all-action-runs) |
| [List Blueprint Entities](actions/list-blueprint-entities.md) | `GET /blueprints/:blueprint_identifier/entities` | [docs](https://docs.port.io/api-reference/get-all-entities-of-a-blueprint) |
| [List Blueprint Scorecards](actions/list-blueprint-scorecards.md) | `GET /blueprints/:blueprint_identifier/scorecards` | [docs](https://docs.port.io/api-reference/get-a-blueprints-scorecards) |
| [List Blueprints](actions/list-blueprints.md) | `GET /blueprints` | [docs](https://docs.port.io/api-reference/get-all-blueprints) |
| [List Credential Sets](actions/list-credential-sets.md) | `GET /apps` | [docs](https://docs.port.io/api-reference/get-all-credentials) |
| [List Integrations](actions/list-integrations.md) | `GET /integration` | [docs](https://docs.port.io/api-reference/get-all-integrations) |
| [List LLM Providers](actions/list-llm-providers.md) | `GET /llm-providers` | [docs](https://docs.port.io/api-reference/get-configured-llm-providers) |
| [List MCP Server Tools](actions/list-mcp-server-tools.md) | `GET /mcp/servers/:server_id/tools` | [docs](https://docs.port.io/api-reference/get-all-tools-for-mcp-server) |
| [List MCP Templates](actions/list-mcp-templates.md) | `GET /mcp/templates` | [docs](https://docs.port.io/api-reference/get-mcp-server-templates) |
| [List MCP User Servers](actions/list-mcp-user-servers.md) | `GET /mcp/user/servers` | [docs](https://docs.port.io/api-reference/get-mcp-servers-for-user) |
| [List Memory Records](actions/list-memory-records.md) | `GET /memory` | [docs](https://docs.port.io/api-reference/list-user-memory-records) |
| [List Migrations](actions/list-migrations.md) | `GET /migrations` | [docs](https://docs.port.io/api-reference/get-all-migrations) |
| [List Organization Secrets](actions/list-organization-secrets.md) | `GET /organization/secrets` | [docs](https://docs.port.io/api-reference/get-all-organization-secrets-metadata) |
| [List Pages](actions/list-pages.md) | `GET /pages` | [docs](https://docs.port.io/api-reference/get-all-pages-in-your-portal) |
| [List Plugins](actions/list-plugins.md) | `GET /plugins` | [docs](https://docs.port.io/api-reference/list-all-plugins-for-the-organization) |
| [List Prompts](actions/list-prompts.md) | `GET /mcp/prompts` | [docs](https://docs.port.io/api-reference/list-available-prompts) |
| [List Scorecards](actions/list-scorecards.md) | `GET /scorecards` | [docs](https://docs.port.io/api-reference/get-all-scorecards) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://docs.port.io/api-reference/get-all-teams-in-your-organization) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.port.io/api-reference/get-all-users-in-your-organization) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.port.io/api-reference/get-all-webhooks) |
| [List Workflow Runs](actions/list-workflow-runs.md) | `GET /workflows/runs` | [docs](https://docs.port.io/api-reference/get-workflow-runs) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://docs.port.io/api-reference/get-workflows) |
| [Rename Blueprint Mirror Property](actions/rename-blueprint-mirror-property.md) | `PATCH /blueprints/:blueprint_identifier/mirror/:property_identifier/rename` | [docs](https://docs.port.io/api-reference/rename-a-blueprints-mirror-property) |
| [Rename Blueprint Property](actions/rename-blueprint-property.md) | `PATCH /blueprints/:blueprint_identifier/properties/:property_identifier/rename` | [docs](https://docs.port.io/api-reference/rename-a-property-in-a-blueprint) |
| [Rename Blueprint Relation](actions/rename-blueprint-relation.md) | `PATCH /blueprints/:blueprint_identifier/relations/:relation_identifier/rename` | [docs](https://docs.port.io/api-reference/rename-a-blueprints-relation) |
| [Review Auto Discovery Suggestions](actions/review-auto-discovery-suggestions.md) | `POST /ai/entities-auto-discovery/:invocation_id/review` | [docs](https://docs.port.io/api-reference/review-auto-discovery-invocation-suggestions) |
| [Rotate User Credentials](actions/rotate-user-credentials.md) | `POST /rotate-credentials/:user_email` | [docs](https://docs.port.io/api-reference/rotate-a-users-credentials) |
| [Search Blueprint Entities](actions/search-blueprint-entities.md) | `POST /blueprints/:blueprint_identifier/entities/search` | [docs](https://docs.port.io/api-reference/search-a-blueprints-entities) |
| [Search Entities](actions/search-entities.md) | `POST /entities/search` | [docs](https://docs.port.io/api-reference/search-entities) |
| [Simulate Blueprint Permissions](actions/simulate-blueprint-permissions.md) | `POST /blueprints/:blueprint_identifier/permissions/simulate` | [docs](https://docs.port.io/api-reference/simulate-permissions-for-a-user) |
| [Start MCP OAuth2 Authentication](actions/start-mcpo-auth2-authentication.md) | `GET /mcp/oauth2/authenticate` | [docs](https://docs.port.io/api-reference/start-mcp-oauth2-authentication) |
| [Submit AI Invocation Feedback](actions/submit-ai-invocation-feedback.md) | `PATCH /ai/invoke/:invocation_identifier/feedback` | [docs](https://docs.port.io/api-reference/submit-ai-invocation-feedback) |
| [Trigger Workflow Run](actions/trigger-workflow-run.md) | `POST /workflows/:workflow_identifier/runs` | [docs](https://docs.port.io/api-reference/trigger-a-workflow-run) |
| [Update Action Automation](actions/update-action-automation.md) | `PUT /actions/:action_identifier` | [docs](https://docs.port.io/api-reference/change-an-action-automation) |
| [Update Action Permissions](actions/update-action-permissions.md) | `PATCH /actions/:action_identifier/permissions` | [docs](https://docs.port.io/api-reference/update-an-actions-permissions) |
| [Update Action Run](actions/update-action-run.md) | `PATCH /actions/runs/:run_id` | [docs](https://docs.port.io/api-reference/update-an-action-run) |
| [Update Auto Discovery Suggestion](actions/update-auto-discovery-suggestion.md) | `PATCH /ai/entities-auto-discovery/:invocation_id/suggestions/:entity_identifier` | [docs](https://docs.port.io/api-reference/update-auto-discovery-invocation-suggestion) |
| [Update Blueprint](actions/update-blueprint.md) | `PATCH /blueprints/:identifier` | [docs](https://docs.port.io/api-reference/update-a-blueprint) |
| [Update Blueprint Permissions](actions/update-blueprint-permissions.md) | `PATCH /blueprints/:blueprint_identifier/permissions` | [docs](https://docs.port.io/api-reference/update-a-blueprints-permissions) |
| [Update Credential Set](actions/update-credential-set.md) | `PUT /apps/:id` | [docs](https://docs.port.io/api-reference/change-the-name-of-a-credentials-set) |
| [Update Default LLM Provider](actions/update-default-llm-provider.md) | `PUT /llm-providers/defaults` | [docs](https://docs.port.io/api-reference/change-default-llm-provider-and-model) |
| [Update Entity](actions/update-entity.md) | `PATCH /blueprints/:blueprint_identifier/entities/:entity_identifier` | [docs](https://docs.port.io/api-reference/update-an-entity) |
| [Update Integration](actions/update-integration.md) | `PATCH /integration/:identifier` | [docs](https://docs.port.io/api-reference/update-an-integration) |
| [Update Integration Config](actions/update-integration-config.md) | `PATCH /integration/:identifier/config` | [docs](https://docs.port.io/api-reference/update-an-integrations-config) |
| [Update LLM Provider](actions/update-llm-provider.md) | `PUT /llm-providers/:provider` | [docs](https://docs.port.io/api-reference/change-a-specific-provider-configuration) |
| [Update Memory Settings](actions/update-memory-settings.md) | `PUT /memory/settings` | [docs](https://docs.port.io/api-reference/update-memory-settings) |
| [Update Organization](actions/update-organization.md) | `PATCH /organization` | [docs](https://docs.port.io/api-reference/update-organization-details) |
| [Update Organization Secret](actions/update-organization-secret.md) | `PATCH /organization/secrets/:secret_name` | [docs](https://docs.port.io/api-reference/update-an-organization-secret) |
| [Update Page Permissions](actions/update-page-permissions.md) | `PATCH /pages/:page_identifier/permissions` | [docs](https://docs.port.io/api-reference/update-a-pages-permissions) |
| [Update Page Widget](actions/update-page-widget.md) | `PATCH /pages/:page_identifier/widgets/:widget_id` | [docs](https://docs.port.io/api-reference/update-a-widget) |
| [Update Plugin Metadata](actions/update-plugin-metadata.md) | `PATCH /plugins/:identifier` | [docs](https://docs.port.io/api-reference/update-metadata-of-a-plugin) |
| [Update Scorecard](actions/update-scorecard.md) | `PUT /blueprints/:blueprint_identifier/scorecards/:scorecard_identifier` | [docs](https://docs.port.io/api-reference/change-a-scorecard) |
| [Update Team](actions/update-team.md) | `PATCH /teams/:name` | [docs](https://docs.port.io/api-reference/update-a-team) |
| [Update User](actions/update-user.md) | `PATCH /users/:user_email` | [docs](https://docs.port.io/api-reference/update-a-user) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /webhooks/:identifier` | [docs](https://docs.port.io/api-reference/update-a-webhook) |
| [Update Workflow](actions/update-workflow.md) | `PUT /workflows/:workflow_identifier` | [docs](https://docs.port.io/api-reference/change-a-workflow) |
| [Update Workflow Node Permissions](actions/update-workflow-node-permissions.md) | `PATCH /workflows/:workflow_identifier/nodes/:node_identifier/permissions` | [docs](https://docs.port.io/api-reference/update-a-workflows-node-permissions) |
| [Update Workflow Node Run](actions/update-workflow-node-run.md) | `PATCH /workflows/nodes/runs/:node_run_identifier` | [docs](https://docs.port.io/api-reference/update-a-workflow-node-run) |
