# <img src="https://images.mindcloud.co/apps/icons/callingly_1782742288271.png" alt="Callingly logo" width="28" height="28"> Callingly: Universal API

Call, text, and route inbound leads for your sales team

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/callingly/latest
- **Category:** Support / Contact Center
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://callingly.com
- **Vendor API docs:** https://help.callingly.com/article/38-callingly-api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Create Call](actions/create-call.md) | POST | Creates a call in Callingly. |
| [Get Call](actions/get-call.md) | GET | Retrieves a call from Callingly. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from Callingly. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a client in Callingly. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes a client from Callingly. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Callingly. |
| [Set Client Active Status](actions/set-client-active-status.md) | PUT | Updates a client's active status in Callingly. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Delete Lead](actions/delete-lead.md) | DELETE | Deletes a lead from Callingly. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from Callingly. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from Callingly. |
| [Update Lead](actions/update-lead.md) | PUT | Updates a lead in Callingly. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Creates a team in Callingly. |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from Callingly. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Callingly. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Team Agents](actions/list-team-agents.md) | GET | Retrieves team agents from Callingly. |
| [Remove Team Agent](actions/remove-team-agent.md) | DELETE | Deletes a team agent from Callingly. |
| [Replace Team Agents](actions/replace-team-agents.md) | PUT | Updates team agents in Callingly. |
| [Update Team Agent Settings](actions/update-team-agent-settings.md) | PUT | Updates team agent settings in Callingly. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates an agent in Callingly. |
| [Get Agent Schedule](actions/get-agent-schedule.md) | GET | Retrieves an agent schedule from Callingly. |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents from Callingly. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an agent in Callingly. |
| [Update Agent Schedule](actions/update-agent-schedule.md) | PUT | Updates an agent schedule in Callingly. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Callingly. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Callingly. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Callingly. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Callingly. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates a webhook in Callingly. |

