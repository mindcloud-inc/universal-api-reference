# <img src="https://images.mindcloud.co/apps/icons/mihu-ai_1775832698645.png" alt="Mihu AI logo" width="28" height="28"> Mihu AI: Universal API

Mihu AI is an AI contact center platform for voice calls, campaigns, contacts, scheduling, tasks, and transcriptions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mihuAI/latest
- **Category:** Support / Contact Center
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mihu.ai
- **Vendor API docs:** https://developers.mihu.ai/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Paginated List of Calls](actions/get-paginated-list-of-calls.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-paginated-list-of-calls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Create a New Appointment](actions/create-a-new-appointment.md) | POST |  |
| [Delete an Appointment](actions/delete-an-appointment.md) | DELETE |  |
| [Get a Specific Appointment](actions/get-a-specific-appointment.md) | GET |  |
| [Get All Appointments (Calendar)](actions/get-all-appointments-calendar.md) | GET |  |
| [Update an Appointment](actions/update-an-appointment.md) | PUT |  |
| [Update Appointment Status](actions/update-appointment-status.md) | PUT |  |

### Appointment Request

| Action | Method | Description |
| --- | --- | --- |
| [Cancel an Appointment Request](actions/cancel-an-appointment-request.md) | PUT |  |
| [Create a New Appointment Request](actions/create-a-new-appointment-request.md) | POST |  |
| [Get a Specific Appointment Request](actions/get-a-specific-appointment-request.md) | GET |  |
| [Get List of Appointment Requests](actions/get-list-of-appointment-requests.md) | GET |  |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Details by UUID](actions/get-call-details-by-uuid.md) | GET |  |
| [Get Paginated List of Calls](actions/get-paginated-list-of-calls.md) | GET |  |
| [Initiate a New Call](actions/initiate-a-new-call.md) | POST |  |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create a New Campaign](actions/create-a-new-campaign.md) | POST |  |
| [Delete a Campaign](actions/delete-a-campaign.md) | DELETE |  |
| [Get Campaign Details](actions/get-campaign-details.md) | GET |  |
| [Get Paginated List of Campaigns](actions/get-paginated-list-of-campaigns.md) | GET |  |
| [Update a Campaign](actions/update-a-campaign.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag to Contact](actions/add-tag-to-contact.md) | PUT |  |
| [Create a New Contact](actions/create-a-new-contact.md) | POST |  |
| [Delete a Contact](actions/delete-a-contact.md) | DELETE |  |
| [Get Contact Details](actions/get-contact-details.md) | GET |  |
| [Get Paginated List of Contacts](actions/get-paginated-list-of-contacts.md) | GET |  |
| [Remove Tag from Contact](actions/remove-tag-from-contact.md) | PUT |  |
| [Update a Contact](actions/update-a-contact.md) | PUT |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Create a New Schedule](actions/create-a-new-schedule.md) | POST |  |
| [Get a Specific Schedule](actions/get-a-specific-schedule.md) | GET |  |
| [Get All Schedules](actions/get-all-schedules.md) | GET |  |
| [Update a Schedule](actions/update-a-schedule.md) | PUT |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Cancel a Task](actions/cancel-a-task.md) | PUT |  |
| [Create a New Task](actions/create-a-new-task.md) | POST |  |
| [Delete a Task](actions/delete-a-task.md) | DELETE |  |
| [Get a Specific Task](actions/get-a-specific-task.md) | GET |  |
| [Get Paginated List of Tasks](actions/get-paginated-list-of-tasks.md) | GET |  |
| [Queue a Task for Execution](actions/queue-a-task-for-execution.md) | PUT |  |
| [Retry a Failed Task](actions/retry-a-failed-task.md) | PUT |  |
| [Update a Task](actions/update-a-task.md) | PUT |  |

### Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Create a New Transcription Request](actions/create-a-new-transcription-request.md) | POST |  |
| [Get Full Transcript with Conversation Messages and Evaluations](actions/get-full-transcript-with-conversation-messages-and-evaluations.md) | GET |  |
| [Get Transcription by UUID](actions/get-transcription-by-uuid.md) | GET |  |

