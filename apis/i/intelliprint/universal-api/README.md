# <img src="https://images.mindcloud.co/apps/icons/intelliprint-favicon_1775059587469.png" alt="Intelliprint logo" width="28" height="28"> Intelliprint: Universal API

Send letters, postcards, mailing lists, and reusable print backgrounds through the Intelliprint API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/intelliprint/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://intelliprint.net
- **Vendor API docs:** https://docs.intelliprint.net/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Backgrounds](actions/list-backgrounds.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/list-backgrounds?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Background

| Action | Method | Description |
| --- | --- | --- |
| [Create Background](actions/create-background.md) | POST |  |
| [Delete Background](actions/delete-background.md) | DELETE |  |
| [List Backgrounds](actions/list-backgrounds.md) | GET |  |
| [Retrieve Background](actions/retrieve-background.md) | GET |  |
| [Update Background](actions/update-background.md) | PUT |  |

### Mailing List

| Action | Method | Description |
| --- | --- | --- |
| [Create Mailing List](actions/create-mailing-list.md) | POST |  |
| [Delete Mailing List](actions/delete-mailing-list.md) | DELETE |  |
| [List Mailing Lists](actions/list-mailing-lists.md) | GET |  |
| [Retrieve Mailing List](actions/retrieve-mailing-list.md) | GET |  |
| [Update Mailing List](actions/update-mailing-list.md) | PUT |  |

### Mailing List Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Create Mailing List Recipient](actions/create-mailing-list-recipient.md) | POST |  |
| [Delete Mailing List Recipient](actions/delete-mailing-list-recipient.md) | DELETE |  |
| [List Mailing List Recipients](actions/list-mailing-list-recipients.md) | GET |  |
| [Retrieve Mailing List Recipient](actions/retrieve-mailing-list-recipient.md) | GET |  |
| [Update Mailing List Recipient](actions/update-mailing-list-recipient.md) | PUT |  |

### Print Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Print Job](actions/create-print-job.md) | POST |  |
| [Delete Print Job](actions/delete-print-job.md) | DELETE |  |
| [List Print Jobs](actions/list-print-jobs.md) | GET |  |
| [Retrieve Print Job](actions/retrieve-print-job.md) | GET |  |
| [Update Print Job](actions/update-print-job.md) | PUT |  |

