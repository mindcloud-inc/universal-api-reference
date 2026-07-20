# <img src="https://images.mindcloud.co/apps/icons/lulu_1775166176786.png" alt="Lulu logo" width="28" height="28"> Lulu: Universal API

Lulu Print API for print-job creation, pricing, file validation, shipping options, and webhook management across Lulu production and sandbox environments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lulu/latest
- **Category:** Commerce
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lulu.com
- **Vendor API docs:** https://api.lulu.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Print Jobs](actions/list-print-jobs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/list-print-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Cover Dimensions](actions/calculate-cover-dimensions.md) | GET | Calculates cover dimensions in Lulu. |
| [Get Cover Validation](actions/get-cover-validation.md) | GET | Retrieves a cover validation record from Lulu. |
| [Get Interior Validation](actions/get-interior-validation.md) | GET | Retrieves an interior validation record from Lulu. |
| [Validate Cover](actions/validate-cover.md) | POST | Validates a cover file in Lulu. |
| [Validate Interior](actions/validate-interior.md) | POST | Validates an interior file in Lulu. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Print Job](actions/cancel-print-job.md) | DELETE | Cancels a print job in Lulu. |
| [Create Print Job](actions/create-print-job.md) | POST | Creates a new print job in Lulu. |
| [Get Print Job](actions/get-print-job.md) | GET | Retrieves a print job from Lulu. |
| [List Print Jobs](actions/list-print-jobs.md) | GET | Retrieves print jobs from Lulu. |
| [Reprint Print Job](actions/reprint-print-job.md) | POST | Creates a reprint of a print job in Lulu. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [Create Print Job Cost Calculation](actions/create-print-job-cost-calculation.md) | GET | Calculates print job costs in Lulu. |
| [Get Print Job Costs](actions/get-print-job-costs.md) | GET | Retrieves costs for a print job from Lulu. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Print Job Statistics](actions/get-print-job-statistics.md) | GET | Retrieves print job statistics from Lulu. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipping Options](actions/get-shipping-options.md) | GET | Retrieves shipping options from Lulu. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Print Job Status](actions/get-print-job-status.md) | GET | Retrieves the status of a print job from Lulu. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Lulu. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Lulu. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Lulu. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Lulu. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Lulu. |

### Webhook Events

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Submissions](actions/list-webhook-submissions.md) | GET | Retrieves webhook submissions from Lulu. |
| [Test Webhook Submission](actions/test-webhook-submission.md) | POST | Creates a test webhook submission in Lulu. |

