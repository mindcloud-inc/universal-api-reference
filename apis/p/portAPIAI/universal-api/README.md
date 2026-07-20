# <img src="https://images.mindcloud.co/apps/icons/port-api-ai-icon_1775758600565.png" alt="Port API AI logo" width="28" height="28"> Port API AI: Universal API

Port API AI wraps the Port API for catalog, blueprints, entities, scorecards, actions, teams, users, audit, integrations, AI, memory, and organization workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/portAPIAI/latest
- **Actions:** 147
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://port.io
- **Vendor API docs:** https://docs.port.io/api-reference/port-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Blueprints](actions/list-blueprints.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/list-blueprints?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (147)

### Action Automation

| Action | Method | Description |
| --- | --- | --- |
| [Create Action Automation](actions/create-action-automation.md) | POST | Creates an action automation in Port. |
| [Delete Action Automation](actions/delete-action-automation.md) | DELETE | Deletes an action automation from Port. |
| [Get Action Automation](actions/get-action-automation.md) | GET | Retrieves an action automation from Port. |
| [List Action Automations](actions/list-action-automations.md) | GET | Retrieves action automations from Port. |
| [Update Action Automation](actions/update-action-automation.md) | PUT | Updates an action automation in Port. |

### Action Permission

| Action | Method | Description |
| --- | --- | --- |
| [Get Action Permissions](actions/get-action-permissions.md) | GET | Retrieves action permissions from Port. |
| [Update Action Permissions](actions/update-action-permissions.md) | PUT | Updates action permissions in Port. |

### Action Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Action Run](actions/get-action-run.md) | GET | Retrieves an action run from Port. |
| [List Action Runs](actions/list-action-runs.md) | GET | Retrieves action runs from Port. |
| [Update Action Run](actions/update-action-run.md) | PUT | Updates an action run in Port. |

### Action Run Approval

| Action | Method | Description |
| --- | --- | --- |
| [Approve Action Run](actions/approve-action-run.md) | PUT | Approves an action run in Port. |

### Action Run Log

| Action | Method | Description |
| --- | --- | --- |
| [Add Action Run Log](actions/add-action-run-log.md) | POST | Creates an action run log in Port. |
| [Get Action Run Logs](actions/get-action-run-logs.md) | GET | Retrieves action run logs from Port. |

### Aggregation Result

| Action | Method | Description |
| --- | --- | --- |
| [Aggregate Entities](actions/aggregate-entities.md) | GET | Retrieves aggregated entities from Port. |
| [Aggregate Entities Over Time](actions/aggregate-entities-over-time.md) | GET | Retrieves entity aggregates over time from Port. |

### Ai Invocation

| Action | Method | Description |
| --- | --- | --- |
| [Get AI Invocation](actions/get-ai-invocation.md) | GET | Retrieves an AI invocation from Port. |
| [Invoke AI](actions/invoke-ai.md) | POST | Creates a general-purpose AI interaction in Port. |

### Ai Invocation Quota

| Action | Method | Description |
| --- | --- | --- |
| [Get AI Invocation Quota](actions/get-ai-invocation-quota.md) | GET | Retrieves AI invocation quota usage from Port. |

### Approvals

| Action | Method | Description |
| --- | --- | --- |
| [List Action Run Approvers](actions/list-action-run-approvers.md) | GET | Retrieves action run approvers from Port. |

### Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Audit Logs](actions/get-audit-logs.md) | GET | Retrieves audit logs from Port. |

### Auto Discovery Invocation

| Action | Method | Description |
| --- | --- | --- |
| [Create Auto Discovery Invocation](actions/create-auto-discovery-invocation.md) | POST | Creates an auto-discovery invocation in Port. |
| [Get Latest Auto Discovery Invocation](actions/get-latest-auto-discovery-invocation.md) | GET |  |

### Auto Discovery Review

| Action | Method | Description |
| --- | --- | --- |
| [Review Auto Discovery Suggestions](actions/review-auto-discovery-suggestions.md) | PUT | Reviews auto-discovery suggestions in Port. |

### Auto Discovery Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Get Auto Discovery Suggestions](actions/get-auto-discovery-suggestions.md) | GET |  |
| [Update Auto Discovery Suggestion](actions/update-auto-discovery-suggestion.md) | PUT |  |

### Blueprint

| Action | Method | Description |
| --- | --- | --- |
| [Create Blueprint](actions/create-blueprint.md) | POST | Creates a blueprint in Port. |
| [Delete Blueprint](actions/delete-blueprint.md) | DELETE | Deletes a blueprint from Port. |
| [Get Blueprint](actions/get-blueprint.md) | GET | Retrieves a blueprint from Port. |
| [List Blueprints](actions/list-blueprints.md) | GET | Retrieves blueprints from Port. |
| [Update Blueprint](actions/update-blueprint.md) | PUT | Updates a blueprint in Port. |

### Blueprint Entity Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Blueprint Entity Count](actions/get-blueprint-entity-count.md) | GET | Retrieves a blueprint's entity count from Port. |

### Blueprint Mirror Property

| Action | Method | Description |
| --- | --- | --- |
| [Rename Blueprint Mirror Property](actions/rename-blueprint-mirror-property.md) | PUT | Updates a blueprint mirror property name in Port. |

### Blueprint Permission

| Action | Method | Description |
| --- | --- | --- |
| [Get Blueprint Permissions](actions/get-blueprint-permissions.md) | GET | Retrieves blueprint permissions from Port. |
| [Update Blueprint Permissions](actions/update-blueprint-permissions.md) | PUT | Updates blueprint permissions in Port. |

### Blueprint Property

| Action | Method | Description |
| --- | --- | --- |
| [Rename Blueprint Property](actions/rename-blueprint-property.md) | PUT | Updates a blueprint property name in Port. |

### Blueprint Relation

| Action | Method | Description |
| --- | --- | --- |
| [Rename Blueprint Relation](actions/rename-blueprint-relation.md) | PUT | Updates a blueprint relation name in Port. |

### Credential Rotation

| Action | Method | Description |
| --- | --- | --- |
| [Rotate User Credentials](actions/rotate-user-credentials.md) | POST | Creates rotated credentials for a user in Port. |

### Credential Set

| Action | Method | Description |
| --- | --- | --- |
| [Create Credential Set](actions/create-credential-set.md) | POST |  |
| [Delete Credential Set](actions/delete-credential-set.md) | DELETE | Deletes a credential set from Port. |
| [List Credential Sets](actions/list-credential-sets.md) | GET | Retrieves credential sets from Port. |
| [Update Credential Set](actions/update-credential-set.md) | PUT | Updates a credential set in Port. |

### Entity

| Action | Method | Description |
| --- | --- | --- |
| [Create Entity](actions/create-entity.md) | POST | Creates an entity in Port. |
| [Create Multiple Entities](actions/create-multiple-entities.md) | POST | Creates multiple entities in Port. |
| [Delete Entity](actions/delete-entity.md) | DELETE | Deletes an entity from Port. |
| [Delete Multiple Entities](actions/delete-multiple-entities.md) | DELETE | Deletes multiple entities from Port. |
| [Get Entity](actions/get-entity.md) | GET | Retrieves an entity from Port. |
| [List Blueprint Entities](actions/list-blueprint-entities.md) | GET | Retrieves entities from a Port blueprint. |
| [Update Entity](actions/update-entity.md) | PUT | Updates an entity in Port. |

### Entity Property History

| Action | Method | Description |
| --- | --- | --- |
| [Get Entity Properties History](actions/get-entity-properties-history.md) | GET | Retrieves entity property history from Port. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Delete Integration](actions/delete-integration.md) | DELETE | Deletes an integration from Port. |
| [Get Integration](actions/get-integration.md) | GET | Retrieves an integration from Port. |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves integrations from Port. |
| [Update Integration](actions/update-integration.md) | PUT | Updates an integration in Port. |
| [Update Integration Config](actions/update-integration-config.md) | PUT | Updates integration configuration in Port. |

### Integration Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration Logs](actions/get-integration-logs.md) | GET | Retrieves integration logs from Port. |

### Integration Sync Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration Sync Metadata](actions/get-integration-sync-metadata.md) | GET | Retrieves integration sync metadata from Port. |

### Integration Sync Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration Sync Metrics](actions/get-integration-sync-metrics.md) | GET | Retrieves integration sync metrics from Port. |

### Llm Provider

| Action | Method | Description |
| --- | --- | --- |
| [Create LLM Provider](actions/create-llm-provider.md) | POST | Creates an LLM provider in Port. |
| [Delete LLM Provider](actions/delete-llm-provider.md) | DELETE | Deletes an LLM provider from Port. |
| [Get LLM Provider](actions/get-llm-provider.md) | GET | Retrieves an LLM provider from Port. |
| [List LLM Providers](actions/list-llm-providers.md) | GET | Retrieves LLM providers from Port. |
| [Update LLM Provider](actions/update-llm-provider.md) | PUT | Updates an LLM provider in Port. |

### Llm Provider Default

| Action | Method | Description |
| --- | --- | --- |
| [Get Default LLM Provider](actions/get-default-llm-provider.md) | GET | Retrieves the default LLM provider from Port. |
| [Update Default LLM Provider](actions/update-default-llm-provider.md) | PUT | Updates the default LLM provider in Port. |

### Mcp Server

| Action | Method | Description |
| --- | --- | --- |
| [Disconnect MCP User Server](actions/disconnect-mcp-user-server.md) | DELETE | Disconnects an MCP user server from Port. |
| [Get MCP User Server](actions/get-mcp-user-server.md) | GET | Retrieves an MCP user server from Port. |
| [List MCP User Servers](actions/list-mcp-user-servers.md) | GET | Retrieves MCP user servers from Port. |

### Mcp Template

| Action | Method | Description |
| --- | --- | --- |
| [List MCP Templates](actions/list-mcp-templates.md) | GET | Retrieves MCP server templates from Port. |

### Mcp Tool

| Action | Method | Description |
| --- | --- | --- |
| [List MCP Server Tools](actions/list-mcp-server-tools.md) | GET | Retrieves MCP server tools from Port. |

### Mcp Tool Call

| Action | Method | Description |
| --- | --- | --- |
| [Call MCP Server Tool](actions/call-mcp-server-tool.md) | POST | Calls an MCP server tool in Port. |

### Memory Record

| Action | Method | Description |
| --- | --- | --- |
| [Delete Memory Records](actions/delete-memory-records.md) | DELETE |  |
| [List Memory Records](actions/list-memory-records.md) | GET |  |

### Memory Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Memory Settings](actions/get-memory-settings.md) | GET | Retrieves memory settings from Port. |
| [Update Memory Settings](actions/update-memory-settings.md) | PUT | Updates memory settings in Port. |

### Migration

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Migration](actions/cancel-migration.md) | PUT | Cancels a migration in Port. |
| [Create Migration](actions/create-migration.md) | POST | Creates a migration in Port. |
| [Get Migration](actions/get-migration.md) | GET | Retrieves a migration from Port. |
| [List Migrations](actions/list-migrations.md) | GET | Retrieves migrations from Port. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves organization details from Port. |
| [Update Organization](actions/update-organization.md) | PUT | Updates organization details in Port. |

### Organization Secret

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization Secret](actions/create-organization-secret.md) | POST | Creates an organization secret in Port. |
| [Delete Organization Secret](actions/delete-organization-secret.md) | DELETE | Deletes an organization secret from Port. |
| [Get Organization Secret](actions/get-organization-secret.md) | GET | Retrieves organization secret metadata from Port. |
| [List Organization Secrets](actions/list-organization-secrets.md) | GET | Retrieves organization secret metadata from Port. |
| [Update Organization Secret](actions/update-organization-secret.md) | PUT | Updates an organization secret in Port. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Delete Page](actions/delete-page.md) | DELETE |  |
| [Get Page](actions/get-page.md) | GET |  |
| [List Pages](actions/list-pages.md) | GET |  |

### Page Permission

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Permissions](actions/get-page-permissions.md) | GET |  |
| [Update Page Permissions](actions/update-page-permissions.md) | PUT |  |

### Permission Simulation

| Action | Method | Description |
| --- | --- | --- |
| [Simulate Blueprint Permissions](actions/simulate-blueprint-permissions.md) | GET | Retrieves simulated blueprint permissions from Port. |

### Plugin

| Action | Method | Description |
| --- | --- | --- |
| [Delete Plugin](actions/delete-plugin.md) | DELETE | Deletes a plugin from Port. |
| [Get Plugin](actions/get-plugin.md) | GET | Retrieves a plugin from Port. |
| [List Plugins](actions/list-plugins.md) | GET | Retrieves plugins from Port. |
| [Update Plugin Metadata](actions/update-plugin-metadata.md) | PUT | Updates plugin metadata in Port. |

### Plugin Upload

| Action | Method | Description |
| --- | --- | --- |
| [Finalize Plugin Upload](actions/finalize-plugin-upload.md) | POST | Finalizes a plugin upload in Port. |
| [Get Plugin Update Upload URL](actions/get-plugin-update-upload-url.md) | PUT | Retrieves a plugin update upload URL from Port. |
| [Get Plugin Upload URL](actions/get-plugin-upload-url.md) | POST | Retrieves a plugin upload URL from Port. |

### Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Get Prompt](actions/get-prompt.md) | GET | Retrieves a prompt from Port. |
| [List Prompts](actions/list-prompts.md) | GET | Retrieves prompts from Port. |

### Scorecard

| Action | Method | Description |
| --- | --- | --- |
| [Create Scorecard](actions/create-scorecard.md) | POST | Creates a scorecard in Port. |
| [Delete Scorecard](actions/delete-scorecard.md) | DELETE | Deletes a scorecard from Port. |
| [Get Scorecard](actions/get-scorecard.md) | GET | Retrieves a scorecard from Port. |
| [List Blueprint Scorecards](actions/list-blueprint-scorecards.md) | GET | Retrieves scorecards for a Port blueprint. |
| [List Scorecards](actions/list-scorecards.md) | GET | Retrieves scorecards from Port. |
| [Update Scorecard](actions/update-scorecard.md) | PUT | Updates a scorecard in Port. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Blueprint Entities](actions/search-blueprint-entities.md) | GET | Finds entities in a Port blueprint. |
| [Search Entities](actions/search-entities.md) | GET | Finds entities in Port. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Creates a team in Port. |
| [Delete Team](actions/delete-team.md) | DELETE | Deletes a team from Port. |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from Port. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Port. |
| [Update Team](actions/update-team.md) | PUT | Updates a team in Port. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Delete AI Invocation Feedback](actions/delete-ai-invocation-feedback.md) | DELETE |  |
| [Delete Memory Users](actions/delete-memory-users.md) | DELETE |  |
| [Delete Page Widget](actions/delete-page-widget.md) | DELETE |  |
| [Get Integration Metadata](actions/get-integration-metadata.md) | GET | Retrieves integration metadata from Port. |
| [Get MCP OAuth2 Session Token](actions/get-mcpo-auth2-session-token.md) | GET |  |
| [Get Webhook Metadata](actions/get-webhook-metadata.md) | GET | Retrieves webhook metadata from Port. |
| [Get Workflow Node](actions/get-workflow-node.md) | GET | Retrieves a workflow node from Port. |
| [Handle MCP OAuth2 Callback](actions/handle-mcpo-auth2-callback.md) | POST |  |
| [Start MCP OAuth2 Authentication](actions/start-mcpo-auth2-authentication.md) | POST |  |
| [Submit AI Invocation Feedback](actions/submit-ai-invocation-feedback.md) | PUT |  |
| [Update Page Widget](actions/update-page-widget.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from Port. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Port. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Port. |
| [Update User](actions/update-user.md) | PUT | Updates a user in Port. |

### User Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Invite User](actions/invite-user.md) | POST | Invites a user to Port. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Port. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Port. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Port. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Port. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates a webhook in Port. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST | Creates a workflow in Port. |
| [Delete Workflow](actions/delete-workflow.md) | DELETE | Deletes a workflow from Port. |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves a workflow from Port. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from Port. |
| [Update Workflow](actions/update-workflow.md) | PUT | Updates a workflow in Port. |

### Workflow Node Permission

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow Node Permissions](actions/create-workflow-node-permissions.md) | POST |  |
| [Delete Workflow Node Permissions](actions/delete-workflow-node-permissions.md) | DELETE |  |
| [Get Workflow Node Permissions](actions/get-workflow-node-permissions.md) | GET |  |
| [Update Workflow Node Permissions](actions/update-workflow-node-permissions.md) | PUT |  |

### Workflow Node Run

| Action | Method | Description |
| --- | --- | --- |
| [Update Workflow Node Run](actions/update-workflow-node-run.md) | PUT | Updates a workflow node run in Port. |

### Workflow Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Run](actions/get-workflow-run.md) | GET | Retrieves a workflow run from Port. |
| [List Workflow Runs](actions/list-workflow-runs.md) | GET | Retrieves workflow runs from Port. |
| [Trigger Workflow Run](actions/trigger-workflow-run.md) | POST | Creates a workflow run in Port. |

