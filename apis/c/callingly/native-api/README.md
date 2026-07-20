# Callingly: Native API Reference

A consolidated summary of Callingly's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://help.callingly.com/article/38-callingly-api-documentation
- **API base URL:** `https://api.callingly.com`

## Authentication

### API Key

Authenticate with a Callingly bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.callingly.com/article/38-callingly-api-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | `POST /v1/agents` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#create-agent) |
| [Create Call](actions/create-call.md) | `POST /v1/calls` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#create-call) |
| [Create Client](actions/create-client.md) | `POST /v1/clients` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#create-client) |
| [Create Team](actions/create-team.md) | `POST /v1/teams` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#create-team) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/webhooks` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#Create-a-Webhook-fv07m) |
| [Delete Client](actions/delete-client.md) | `DELETE /v1/clients/{{id}}` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#delete-client) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /v1/leads/{{id}}` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#Delete-Lead-WgweT) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v1/webhooks/{{id}}` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#Delete-a-Webhook-GyGhB) |
| [Get Agent Schedule](actions/get-agent-schedule.md) | `GET /v1/agents/{{id}}/schedule` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#get-agent-schedule) |
| [Get Call](actions/get-call.md) | `GET /v1/calls/{{id}}` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#Get-Call-JlDGl) |
| [Get Lead](actions/get-lead.md) | `GET /v1/leads/{{id}}` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#Get-Lead-vwwS6) |
| [Get Team](actions/get-team.md) | `GET /v1/teams/{{id}}` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#get-team) |
| [Get Webhook](actions/get-webhook.md) | `GET /v1/webhooks/{{id}}` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#Get-a-Webhook-iB9fR) |
| [List Agents](actions/list-agents.md) | `GET /v1/agents` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#list-users) |
| [List Calls](actions/list-calls.md) | `GET /v1/calls` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#list-calls) |
| [List Clients](actions/list-clients.md) | `GET /v1/clients` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#list-clients) |
| [List Leads](actions/list-leads.md) | `GET /v1/leads` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#List-Leads-_hyZk) |
| [List Team Agents](actions/list-team-agents.md) | `GET /v1/teams/{{id}}/agents` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#list-team-users) |
| [List Teams](actions/list-teams.md) | `GET /v1/teams` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#list-teams) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/webhooks` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#List-All-Webhooks-vkO9i) |
| [Remove Team Agent](actions/remove-team-agent.md) | `DELETE /v1/teams/{{id}}/agents/{{agent_id}}` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#remove-agents) |
| [Replace Team Agents](actions/replace-team-agents.md) | `PUT /v1/teams/{{id}}/agents` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#update-users) |
| [Set Client Active Status](actions/set-client-active-status.md) | `POST /v1/clients/{{id}}/active` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#activate-deactivate) |
| [Update Agent](actions/update-agent.md) | `PUT /v1/agents/{{id}}` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#update-agent) |
| [Update Agent Schedule](actions/update-agent-schedule.md) | `PUT /v1/agents/{{id}}/schedule` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#update-schedule) |
| [Update Lead](actions/update-lead.md) | `PUT /v1/leads/{{id}}` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#Update-Agent-sx_cL) |
| [Update Team Agent Settings](actions/update-team-agent-settings.md) | `PUT /v1/teams/{{id}}/agents/{{agent_id}}` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#update-agent-settings) |
| [Update Webhook](actions/update-webhook.md) | `PUT /v1/webhooks/{{webhookId}}` | [docs](https://help.callingly.com/article/38-callingly-api-documentation#Update-a-Webhook-mvgYy) |
