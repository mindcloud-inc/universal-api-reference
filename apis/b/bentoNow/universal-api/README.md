# <img src="https://images.mindcloud.co/apps/icons/bento-logo_1774294001705.png" alt="Bento Now logo" width="28" height="28"> Bento Now: Universal API

Manage Bento subscribers, broadcasts, emails, and engagement events

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bentoNow/latest
- **Category:** Marketing
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bentonow.com
- **Vendor API docs:** https://bentonow.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Tags](actions/get-tags.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/get-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a custom profile field in Bento Now. |
| [Get Fields](actions/get-fields.md) | GET | Retrieves custom fields from Bento Now. |

### Email Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Broadcasts](actions/create-broadcasts.md) | POST | Creates a broadcast campaign in Bento Now. |
| [Get Broadcasts](actions/get-broadcasts.md) | GET | Retrieves broadcast history and metadata from Bento Now. |

### Email Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Sequence Email](actions/create-sequence-email.md) | POST | Creates an email template in a Bento Now sequence. |
| [Get Email Template](actions/get-email-template.md) | GET | Retrieves an email template with stats from Bento Now. |
| [Update Email Template](actions/update-email-template.md) | PUT | Updates an email template subject or HTML in Bento Now. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Create Emails](actions/create-emails.md) | POST | Queues transactional emails in Bento Now. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Events](actions/create-events.md) | POST | Tracks user activity in Bento Now. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Get Segment Stats](actions/get-segment-stats.md) | GET | Retrieves subscriber statistics for a Bento Now segment. |

### Sequence

| Action | Method | Description |
| --- | --- | --- |
| [Get Sequences](actions/get-sequences.md) | GET | Retrieves sequences and email templates from Bento Now. |

### Site Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Stats](actions/get-site-stats.md) | GET | Retrieves site subscriber statistics from Bento Now. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in Bento Now. |
| [Find Subscriber](actions/find-subscriber.md) | GET | Finds a subscriber in Bento Now by email or UUID. |
| [Import Subscribers](actions/import-subscribers.md) | PUT | Imports subscribers into Bento Now without triggering automations. |
| [Run Subscriber Command](actions/run-subscriber-command.md) | PUT | Runs a targeted subscriber command in Bento Now. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a custom tag in Bento Now. |
| [Get Tags](actions/get-tags.md) | GET | Retrieves account tags from Bento Now. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflows](actions/get-workflows.md) | GET | Retrieves workflows and email templates from Bento Now. |

