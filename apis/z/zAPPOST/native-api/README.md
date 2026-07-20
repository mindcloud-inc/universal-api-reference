# ZAP POST: Native API Reference

A consolidated summary of ZAP POST's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://apidocumentation.zappost.com/
- **API base URL:** `https://api.zappost.com`

## Authentication

### Basic Auth

Use your ZAP POST API key as the username and your API password as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://apidocumentation.zappost.com/authentication)

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Batch Submission](actions/create-batch-submission.md) | `POST /api/v1/submissions` | [docs](https://apidocumentation.zappost.com/api-endpoints/submissions) |
| [Create Batch Submission For Specific Scheduled Send](actions/create-batch-submission-for-specific-scheduled-send.md) | `POST /api/v1/submissions` | [docs](https://apidocumentation.zappost.com/api-endpoints/submissions) |
| [Create Batch Submission Valid Records Only](actions/create-batch-submission-valid-records-only.md) | `POST /api/v1/submissions` | [docs](https://apidocumentation.zappost.com/api-endpoints/submissions) |
| [Create Single Record Submission](actions/create-single-record-submission.md) | `POST /api/v1/records` | [docs](https://apidocumentation.zappost.com/api-endpoints/submissions) |
| [Create Single Record Submission For Specific Scheduled Send](actions/create-single-record-submission-for-specific-scheduled-send.md) | `POST /api/v1/records` | [docs](https://apidocumentation.zappost.com/api-endpoints/submissions) |
| [Create Single Record Submission Valid Records Only](actions/create-single-record-submission-valid-records-only.md) | `POST /api/v1/records` | [docs](https://apidocumentation.zappost.com/api-endpoints/submissions) |
| [Get Campaign](actions/get-campaign.md) | `GET /api/v1/campaign/:campaignId` | [docs](https://apidocumentation.zappost.com/api-endpoints/campaigns) |
| [Get Rejected Records For Submission](actions/get-rejected-records-for-submission.md) | `GET /api/v1/RejectedRecords/:submissionId` | [docs](https://apidocumentation.zappost.com/api-endpoints/rejectedrecords) |
| [List Active Submissions For Campaign](actions/list-active-submissions-for-campaign.md) | `GET /api/v1/submissions/Active/:campaignId` | [docs](https://apidocumentation.zappost.com/api-endpoints/submissions) |
| [List Campaigns](actions/list-campaigns.md) | `GET /api/v1/campaigns` | [docs](https://apidocumentation.zappost.com/api-endpoints/campaigns) |
| [List Scheduled Sends](actions/list-scheduled-sends.md) | `GET /api/v1/ScheduledSends` | [docs](https://apidocumentation.zappost.com/api-endpoints/scheduledsends) |
| [List Submissions For Campaign](actions/list-submissions-for-campaign.md) | `GET /api/v1/submissions/:campaignId` | [docs](https://apidocumentation.zappost.com/api-endpoints/submissions) |
