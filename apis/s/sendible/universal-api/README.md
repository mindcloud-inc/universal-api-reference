# <img src="https://images.mindcloud.co/apps/icons/sendible-logo_1774377068418.jpeg" alt="Sendible logo" width="28" height="28"> Sendible: Universal API

Manage social publishing, media, campaigns, and reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sendible/latest
- **Category:** Marketing / Social Media
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sendible.com
- **Vendor API docs:** https://support.sendible.com/hc/en-us

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Abort Upload](actions/abort-upload.md) | DELETE |  |
| [Complete Upload](actions/complete-upload.md) | PUT |  |
| [Create Media](actions/create-media.md) | POST |  |
| [Create Upload Intent](actions/create-upload-intent.md) | POST |  |
| [Delete Media](actions/delete-media.md) | DELETE |  |
| [Get Media](actions/get-media.md) | GET |  |
| [List Media](actions/list-media.md) | GET |  |
| [List Recent Media](actions/list-recent-media.md) | GET |  |
| [Rename Media](actions/rename-media.md) | PUT |  |
| [Search Images](actions/search-images.md) | GET |  |

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [List Holidays](actions/list-holidays.md) | GET |  |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET |  |
| [Get Campaign Overview](actions/get-campaign-overview.md) | GET |  |
| [List Campaigns](actions/list-campaigns.md) | GET |  |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |
| [List Accounts](actions/list-accounts.md) | GET |  |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Media Library](actions/create-media-library.md) | POST |  |
| [Delete Media Library](actions/delete-media-library.md) | DELETE |  |
| [List Media Libraries](actions/list-media-libraries.md) | GET |  |
| [Rename Media Library](actions/rename-media-library.md) | PUT |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Generate AI Content Variation](actions/generate-ai-content-variation.md) | GET |  |
| [Generate AI Text](actions/generate-ai-text.md) | GET |  |
| [Get Calendar Message](actions/get-calendar-message.md) | GET |  |
| [List Calendar Messages](actions/list-calendar-messages.md) | GET |  |
| [List Calendar Summary](actions/list-calendar-summary.md) | GET |  |
| [Reschedule Message](actions/reschedule-message.md) | PUT |  |
| [Resolve Message Recipients](actions/resolve-message-recipients.md) | PUT |  |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [List Reminders](actions/list-reminders.md) | GET |  |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Link Preview](actions/get-link-preview.md) | GET |  |

### Queues

| Action | Method | Description |
| --- | --- | --- |
| [List Queues](actions/list-queues.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Audience Report](actions/get-campaign-audience-report.md) | GET |  |
| [Get Campaign Overview Report](actions/get-campaign-overview-report.md) | GET |  |
| [Get Campaign Posts Report](actions/get-campaign-posts-report.md) | GET |  |
| [Get TikTok Report](actions/get-tik-tok-report.md) | GET |  |
| [List Quick Reports](actions/list-quick-reports.md) | GET |  |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Disable Feature Tag](actions/disable-feature-tag.md) | DELETE |  |
| [Enable Feature Tag](actions/enable-feature-tag.md) | POST |  |
| [List Togglable Features](actions/list-togglable-features.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET |  |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [List Filters](actions/list-filters.md) | GET |  |

