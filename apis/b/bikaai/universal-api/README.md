# <img src="https://images.mindcloud.co/apps/icons/bikaai_1776802603651.png" alt="Bika.ai logo" width="28" height="28"> Bika.ai: Universal API

Bika.ai is an AI workflow automation and database platform for spaces, databases, records, attachments, automations, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bikaai/latest
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bika.ai/
- **Vendor API docs:** https://bika.ai/help/guide/developer/openapi

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get System Meta](actions/get-system-meta.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/get-system-meta?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Upload Attachment](actions/upload-attachment.md) | POST | Uploads an attachment to Bika.ai. |

### Automation Trigger

| Action | Method | Description |
| --- | --- | --- |
| [List Automation Triggers](actions/list-automation-triggers.md) | GET |  |

### Database Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Database Record](actions/create-database-record.md) | POST | Creates a database record in Bika.ai. |
| [Delete Database Record](actions/delete-database-record.md) | DELETE | Deletes a database record from Bika.ai. |
| [List Database Records](actions/list-database-records.md) | GET | Retrieves database records from Bika.ai. |
| [Update Database Record](actions/update-database-record.md) | PUT | Updates a database record in Bika.ai. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [List Space Nodes](actions/list-space-nodes.md) | GET | Retrieves nodes from a Bika.ai space. |

### Outbound Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Register Outbound Webhook](actions/register-outbound-webhook.md) | POST | Creates an outbound webhook in Bika.ai. |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves spaces from Bika.ai. |

### System Meta

| Action | Method | Description |
| --- | --- | --- |
| [Get System Meta](actions/get-system-meta.md) | GET | Retrieves system metadata from Bika.ai. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Embed Links](actions/list-embed-links.md) | GET | Retrieves embed links from a Bika.ai space. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves your Bika.ai user profile. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [List Outbound Webhooks](actions/list-outbound-webhooks.md) | GET | Retrieves outbound webhooks from a Bika.ai space. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Space](actions/get-space.md) | GET | Retrieves a space from Bika.ai. |

