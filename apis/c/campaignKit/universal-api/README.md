# <img src="https://images.mindcloud.co/apps/icons/97155797_1781291195734.png" alt="CampaignKit logo" width="28" height="28"> CampaignKit: Universal API

Validate email addresses, run bulk verification jobs, retrieve job results, find professional email addresses, and manage webhook subscriptions in CampaignKit.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/campaignKit/latest
- **Category:** Communication / Email Communications
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://campaignkit.cc
- **Vendor API docs:** https://campaignkit.cc/docs/api/email-validation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Emails](actions/validate-emails.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/validate-emails?connectionId=$CONNECTION_ID&emails%5B%5D=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Find Emails](actions/find-emails.md) | GET | Finds professional email addresses in CampaignKit by name and domain. |
| [Get Validation Job Results](actions/get-validation-job-results.md) | GET | Retrieves paginated validation job results from CampaignKit. |
| [Validate Emails](actions/validate-emails.md) | GET | Validates one or more email addresses in CampaignKit. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download Validation Job Results](actions/download-validation-job-results.md) | GET | Downloads validation job results from CampaignKit as a CSV file. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create Validation Job](actions/create-validation-job.md) | POST | Creates a bulk email validation job in CampaignKit. |
| [Delete Validation Job](actions/delete-validation-job.md) | DELETE | Deletes an existing validation job from CampaignKit. |
| [Get Validation Job](actions/get-validation-job.md) | GET | Retrieves a validation job from CampaignKit by ID. |
| [List Validation Jobs](actions/list-validation-jobs.md) | GET | Retrieves bulk email validation jobs from CampaignKit. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook subscription in CampaignKit. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook subscription from CampaignKit. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook subscription from CampaignKit by ID. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook subscriptions from your CampaignKit account. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook subscription in CampaignKit. |

