# Vibrato: Native API Reference

A consolidated summary of Vibrato's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.getvibrato.com/pages/introduction
- **OpenAPI specification:** https://docs.getvibrato.com/public_api.yaml
- **API base URL:** `https://api.getvibrato.com/api/v1`

## Authentication

### API Key

Authenticate with a Vibrato API token using the Authorization Bearer header.

### Credentials

- **API key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.getvibrato.com/api-reference/campaigns/list-all-campaigns)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `results`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create call](actions/create-call.md) | `POST /calls/` | [docs](https://docs.getvibrato.com/api-reference/calls/create-a-new-call) |
| [Create campaign](actions/create-campaign.md) | `POST /campaigns/` | [docs](https://docs.getvibrato.com/api-reference/campaigns/create-a-new-campaign) |
| [Create contact](actions/create-contact.md) | `POST /contacts/` | [docs](https://docs.getvibrato.com/api-reference/contacts/create-a-new-contact) |
| [Create task template](actions/create-task-template.md) | `POST /task_templates/` | [docs](https://docs.getvibrato.com/api-reference/tasktemplates/create-a-new-task-template) |
| [Create task template from call](actions/create-task-template-from-call.md) | `POST /task_templates/create_from_call/` | [docs](https://docs.getvibrato.com/api-reference/tasktemplates/create-a-task-template-from-a-call) |
| [Delete call](actions/delete-call.md) | `DELETE /calls/{id}/` | [docs](https://docs.getvibrato.com/api-reference/calls/delete-a-specific-call) |
| [Delete campaign](actions/delete-campaign.md) | `DELETE /campaigns/{uuid}/` | [docs](https://docs.getvibrato.com/api-reference/campaigns/delete-a-specific-campaign) |
| [Delete contact](actions/delete-contact.md) | `DELETE /contacts/{uuid}/` | [docs](https://docs.getvibrato.com/api-reference/contacts/delete-a-specific-contact) |
| [Delete task template](actions/delete-task-template.md) | `DELETE /task_templates/{uuid}/` | [docs](https://docs.getvibrato.com/api-reference/tasktemplates/delete-a-specific-task-template) |
| [End call](actions/end-call.md) | `POST /calls/{id}/end/` | [docs](https://docs.getvibrato.com/api-reference/calls/end-a-specific-call) |
| [Get call transcript](actions/get-call-transcript.md) | `GET /calls/{id}/transcript/` | [docs](https://docs.getvibrato.com/api-reference/calls/get-transcript-for-a-specific-call) |
| [List calls](actions/list-calls.md) | `GET /calls/` | [docs](https://docs.getvibrato.com/api-reference/calls/list-all-calls) |
| [List campaigns](actions/list-campaigns.md) | `GET /campaigns/` | [docs](https://docs.getvibrato.com/api-reference/campaigns/list-all-campaigns) |
| [List contacts](actions/list-contacts.md) | `GET /contacts/` | [docs](https://docs.getvibrato.com/api-reference/contacts/list-all-contacts) |
| [List task templates](actions/list-task-templates.md) | `GET /task_templates/` | [docs](https://docs.getvibrato.com/api-reference/tasktemplates/list-all-task-templates) |
| [Retrieve call](actions/retrieve-call.md) | `GET /calls/{id}/` | [docs](https://docs.getvibrato.com/api-reference/calls/retrieve-a-specific-call) |
| [Retrieve campaign](actions/retrieve-campaign.md) | `GET /campaigns/{uuid}/` | [docs](https://docs.getvibrato.com/api-reference/campaigns/retrieve-a-specific-campaign) |
| [Retrieve contact](actions/retrieve-contact.md) | `GET /contacts/{uuid}/` | [docs](https://docs.getvibrato.com/api-reference/contacts/retrieve-a-specific-contact) |
| [Retrieve task template](actions/retrieve-task-template.md) | `GET /task_templates/{uuid}/` | [docs](https://docs.getvibrato.com/api-reference/tasktemplates/retrieve-a-specific-task-template) |
| [Update call](actions/update-call.md) | `PATCH /calls/{id}/` | [docs](https://docs.getvibrato.com/api-reference/calls/update-an-existing-call) |
| [Update campaign](actions/update-campaign.md) | `PATCH /campaigns/{uuid}/` | [docs](https://docs.getvibrato.com/api-reference/campaigns/update-an-existing-campaign) |
| [Update contact](actions/update-contact.md) | `PATCH /contacts/{uuid}/` | [docs](https://docs.getvibrato.com/api-reference/contacts/update-an-existing-contact) |
| [Update task template](actions/update-task-template.md) | `PATCH /task_templates/{uuid}/` | [docs](https://docs.getvibrato.com/api-reference/tasktemplates/update-an-existing-task-template) |
