# <img src="https://images.mindcloud.co/apps/icons/favicon-5_1774021821127.png" alt="Deepgram logo" width="28" height="28"> Deepgram: Universal API

Transcribe speech, generate audio, analyze text, and manage voice agents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deepgram/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.deepgram.com
- **Vendor API docs:** https://developers.deepgram.com/reference/deepgram-api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Token Details](actions/get-token-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Generate Temporary Token](actions/generate-temporary-token.md) | POST | Creates a temporary token in Deepgram. |
| [Get Token Details](actions/get-token-details.md) | GET | Retrieves API token details from Deepgram. |

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Key](actions/create-project-key.md) | POST | Creates a new project API key in Deepgram. |
| [Get Project Key](actions/get-project-key.md) | GET | Retrieves a project API key from Deepgram. |
| [List Project Keys](actions/list-project-keys.md) | GET | Retrieves project API keys from Deepgram. |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [List Project Invites](actions/list-project-invites.md) | GET | Retrieves project invites from Deepgram. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Get Available Model](actions/get-available-model.md) | GET | Retrieves an available model from Deepgram. |
| [Get Project Model](actions/get-project-model.md) | GET | Retrieves a project model from Deepgram. |
| [List All Available Models](actions/list-all-available-models.md) | GET | Retrieves available models from Deepgram. |
| [List Project Models](actions/list-project-models.md) | GET | Retrieves project models from Deepgram. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Project Purchases](actions/list-project-purchases.md) | GET | Retrieves project purchases from Deepgram. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [List Project Member Scopes](actions/list-project-member-scopes.md) | GET | Retrieves project member scopes from Deepgram. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Balance](actions/get-project-balance.md) | GET | Retrieves a project balance from Deepgram. |
| [Get Project Balances](actions/get-project-balances.md) | GET | Retrieves project balances from Deepgram. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Deepgram. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Deepgram. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Billing Breakdown](actions/get-project-billing-breakdown.md) | GET | Retrieves a project billing breakdown from Deepgram. |
| [Get Project Usage](actions/get-project-usage.md) | GET | Retrieves project usage from Deepgram. |
| [Get Project Usage Breakdown](actions/get-project-usage-breakdown.md) | GET | Retrieves a project usage breakdown from Deepgram. |
| [List Project Billing Fields](actions/list-project-billing-fields.md) | GET | Retrieves project billing fields from Deepgram. |
| [List Project Usage Fields](actions/list-project-usage-fields.md) | GET | Retrieves project usage fields from Deepgram. |

### Service Requests

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Request](actions/get-project-request.md) | GET | Retrieves a project request from Deepgram. |
| [List Project Requests](actions/list-project-requests.md) | GET | Retrieves project requests from Deepgram. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Project Members](actions/list-project-members.md) | GET | Retrieves project members from Deepgram. |

