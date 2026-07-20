# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-05-08-as-16_1778269016257.png" alt="Vibrato logo" width="28" height="28"> Vibrato: Universal API

Vibrato provides an API for managing AI phone calls, contacts, reusable task templates, and calling campaigns.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vibrato/latest
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getvibrato.com
- **Vendor API docs:** https://docs.getvibrato.com/pages/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Create call](actions/create-call.md) | POST | Creates a new call in Vibrato. |
| [Delete call](actions/delete-call.md) | DELETE | Deletes an existing call from Vibrato. |
| [End call](actions/end-call.md) | PUT | Ends an existing call in Vibrato. |
| [List calls](actions/list-calls.md) | GET | Retrieves a list of calls from Vibrato. |
| [Retrieve call](actions/retrieve-call.md) | GET | Retrieves a specific call from Vibrato. |
| [Update call](actions/update-call.md) | PUT | Updates an existing call in Vibrato. |

### Call Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Get call transcript](actions/get-call-transcript.md) | GET | Retrieves the transcript for a specific Vibrato call. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create campaign](actions/create-campaign.md) | POST | Creates a new campaign in Vibrato. |
| [Delete campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from Vibrato. |
| [List campaigns](actions/list-campaigns.md) | GET | Retrieves a list of campaigns from Vibrato. |
| [Retrieve campaign](actions/retrieve-campaign.md) | GET | Retrieves a specific campaign from Vibrato. |
| [Update campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Vibrato. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create contact](actions/create-contact.md) | POST | Creates a new contact in Vibrato. |
| [Delete contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Vibrato. |
| [List contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from Vibrato. |
| [Retrieve contact](actions/retrieve-contact.md) | GET | Retrieves a specific contact from Vibrato. |
| [Update contact](actions/update-contact.md) | PUT | Updates an existing contact in Vibrato. |

### Task Template

| Action | Method | Description |
| --- | --- | --- |
| [Create task template](actions/create-task-template.md) | POST | Creates a new task template in Vibrato. |
| [Create task template from call](actions/create-task-template-from-call.md) | POST | Creates a task template from a Vibrato call. |
| [Delete task template](actions/delete-task-template.md) | DELETE | Deletes an existing task template from Vibrato. |
| [List task templates](actions/list-task-templates.md) | GET | Retrieves a list of task templates from Vibrato. |
| [Retrieve task template](actions/retrieve-task-template.md) | GET | Retrieves a specific task template from Vibrato. |
| [Update task template](actions/update-task-template.md) | PUT | Updates an existing task template in Vibrato. |

