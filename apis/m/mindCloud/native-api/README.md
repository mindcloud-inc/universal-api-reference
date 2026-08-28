# MindCloud: Native API Reference

A consolidated summary of MindCloud's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://mindcloud.co/docs/api/rest/introduction
- **OpenAPI specification:** https://connect.mindcloud.co/v2/openapi.json
- **API base URL:** `https://connect.mindcloud.co`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://mindcloud.co/docs/api/rest/introduction/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Run](actions/cancel-run.md) | `POST /v2/runs/:runId/cancel` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Create API Key](actions/create-api-key.md) | `POST /v2/api-keys` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Create Role](actions/create-role.md) | `POST /v2/roles` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Create Workflow](actions/create-workflow.md) | `POST /v2/workflows` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Delete Connection](actions/delete-connection.md) | `DELETE /v2/connections/:connectionId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Delete Role](actions/delete-role.md) | `DELETE /v2/roles/:roleId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Delete Workflow](actions/delete-workflow.md) | `DELETE /v2/workflows/:workflowId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Duplicate Workflow](actions/duplicate-workflow.md) | `POST /v2/workflows/:workflowId/duplicate` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Get Connection](actions/get-connection.md) | `GET /v2/connections/:connectionId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Get Current User](actions/get-current-user.md) | `GET /v2/me` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Get Daily Usage](actions/get-daily-usage.md) | `GET /v2/usage/daily` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Get Role](actions/get-role.md) | `GET /v2/roles/:roleId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Get Run](actions/get-run.md) | `GET /v2/runs/:runId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Get Run Step](actions/get-run-step.md) | `GET /v2/runs/:runId/steps/:stepInstanceId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Get Universal Action](actions/get-universal-action.md) | `GET /v2/universal/apps/:appSlug/actions/:actionSlug` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Get Usage](actions/get-usage.md) | `GET /v2/usage` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Get Workflow](actions/get-workflow.md) | `GET /v2/workflows/:workflowId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Get Workflow Usage](actions/get-workflow-usage.md) | `GET /v2/usage/workflows` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Invite Members](actions/invite-members.md) | `POST /v2/members` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [List API Keys](actions/list-api-keys.md) | `GET /v2/api-keys` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [List Connections](actions/list-connections.md) | `GET /v2/connections` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [List Environments](actions/list-environments.md) | `GET /v2/environments` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [List Members](actions/list-members.md) | `GET /v2/members` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [List Platform Companies](actions/list-platform-companies.md) | `GET /v2/companies` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [List Roles](actions/list-roles.md) | `GET /v2/roles` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [List Run Operations](actions/list-run-operations.md) | `GET /v2/runs/:runId/operations` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [List Run Steps](actions/list-run-steps.md) | `GET /v2/runs/:runId/steps` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [List Universal Actions](actions/list-universal-actions.md) | `GET /v2/universal/apps/:appSlug/actions` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [List Universal Apps](actions/list-universal-apps.md) | `GET /v2/universal/apps` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [List Workflow Runs](actions/list-workflow-runs.md) | `GET /v2/workflows/:workflowId/runs` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [List Workflows](actions/list-workflows.md) | `GET /v2/workflows` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Remove Member](actions/remove-member.md) | `DELETE /v2/members/:userId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Revoke API Key](actions/revoke-api-key.md) | `DELETE /v2/api-keys/:apiKeyId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Run Universal Action](actions/run-universal-action.md) | `POST /v2/universal/apps/:appSlug/actions/:actionSlug/run` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Run Workflow](actions/run-workflow.md) | `POST /v2/workflows/:workflowId/run` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Test Connection](actions/test-connection.md) | `POST /v2/connections/:connectionId/test` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Update Company](actions/update-company.md) | `PATCH /v2/companies/:companyId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Update Member Role](actions/update-member-role.md) | `PUT /v2/members/:userId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Update Role](actions/update-role.md) | `PUT /v2/roles/:roleId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
| [Update Workflow](actions/update-workflow.md) | `PUT /v2/workflows/:workflowId` | [docs](https://connect.mindcloud.co/v2/openapi.json) |
