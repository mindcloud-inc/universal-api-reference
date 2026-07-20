# <img src="https://images.mindcloud.co/apps/icons/apple-touch-icon-3_1775070156671.png" alt="PreCallAI logo" width="28" height="28"> PreCallAI: Universal API

PreCallAI helps teams build, manage, and run AI voice-call workflows with assistants, dialers, segments, campaigns, and call playground tooling.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/preCallAI/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://precallai.com
- **Vendor API docs:** https://docs.precallai.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Assistants](actions/list-assistants.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-assistants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Assistant

| Action | Method | Description |
| --- | --- | --- |
| [Create Assistant](actions/create-assistant.md) | POST | Creates a new assistant in PreCallAI. |
| [Delete Assistant](actions/delete-assistant.md) | DELETE | Deletes an existing assistant from PreCallAI. |
| [List Assistants](actions/list-assistants.md) | GET | Retrieves assistants from PreCallAI. |
| [Update Assistant](actions/update-assistant.md) | PUT | Updates an existing assistant in PreCallAI. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in PreCallAI. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from PreCallAI. |

### Campaign Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Contacts](actions/list-campaign-contacts.md) | GET | Retrieves campaign contacts from PreCallAI. |

### Dialer

| Action | Method | Description |
| --- | --- | --- |
| [Create Dialer](actions/create-dialer.md) | POST | Creates a new dialer in PreCallAI. |
| [Delete Dialer](actions/delete-dialer.md) | DELETE | Deletes an existing dialer from PreCallAI. |
| [List Dialers](actions/list-dialers.md) | GET | Retrieves dialers from PreCallAI. |
| [Update Dialer](actions/update-dialer.md) | PUT | Updates an existing dialer in PreCallAI. |

### Playground Call

| Action | Method | Description |
| --- | --- | --- |
| [Create Playground](actions/create-playground.md) | POST | Creates a new playground in PreCallAI. |
| [List Playgrounds](actions/list-playgrounds.md) | GET | Retrieves playground history from PreCallAI. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST | Creates a new segment in PreCallAI. |
| [Delete Segment](actions/delete-segment.md) | DELETE | Deletes an existing segment from PreCallAI. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from PreCallAI. |
| [Update Segment](actions/update-segment.md) | PUT | Updates an existing segment in PreCallAI. |

### Segment Contact

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Upload Segment Contacts](actions/bulk-upload-segment-contacts.md) | POST | Bulk uploads segment contacts in PreCallAI. |
| [Create Segment Contact](actions/create-segment-contact.md) | POST | Creates a new segment contact in PreCallAI. |
| [Delete Segment Contact](actions/delete-segment-contact.md) | DELETE | Deletes an existing segment contact from PreCallAI. |
| [List Segment Contacts](actions/list-segment-contacts.md) | GET | Retrieves segment contacts from PreCallAI. |
| [Update Segment Contact](actions/update-segment-contact.md) | PUT | Updates an existing segment contact in PreCallAI. |

