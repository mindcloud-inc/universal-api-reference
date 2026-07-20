# <img src="https://images.mindcloud.co/apps/icons/z-appost_1776100812038.png" alt="ZAP POST logo" width="28" height="28"> ZAP POST: Universal API

ZAP POST automates personalised direct mail campaigns by triggering postcards and letters from customer events and scheduled sends.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zAPPOST/latest
- **Category:** Marketing
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zappost.com/
- **Vendor API docs:** https://apidocumentation.zappost.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Scheduled Sends](actions/list-scheduled-sends.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/list-scheduled-sends?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a specific campaign from ZAP POST. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaign list from ZAP POST. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [List Scheduled Sends](actions/list-scheduled-sends.md) | GET | Retrieves scheduled sends from ZAP POST. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch Submission](actions/create-batch-submission.md) | POST | Creates a batch submission in a ZAP POST campaign. |
| [Create Batch Submission For Specific Scheduled Send](actions/create-batch-submission-for-specific-scheduled-send.md) | POST | Creates a batch submission for a specific scheduled send. |
| [Create Batch Submission Valid Records Only](actions/create-batch-submission-valid-records-only.md) | POST | Creates a batch submission using only valid records. |
| [Create Single Record Submission](actions/create-single-record-submission.md) | POST | Creates a single-record submission in a ZAP POST campaign. |
| [Create Single Record Submission For Specific Scheduled Send](actions/create-single-record-submission-for-specific-scheduled-send.md) | POST | Creates a single-record submission for a specific scheduled send. |
| [Create Single Record Submission Valid Records Only](actions/create-single-record-submission-valid-records-only.md) | POST | Creates a single-record submission using only valid records. |
| [Get Rejected Records For Submission](actions/get-rejected-records-for-submission.md) | GET | Retrieves rejected records for a specific submission from ZAP POST. |
| [List Active Submissions For Campaign](actions/list-active-submissions-for-campaign.md) | GET | Retrieves active submissions for a specific campaign from ZAP POST. |
| [List Submissions For Campaign](actions/list-submissions-for-campaign.md) | GET | Retrieves submissions for a specific campaign from ZAP POST. |

