# <img src="https://images.mindcloud.co/apps/icons/snapchat-lead-generation_1774474575784.png" alt="Snapchat Lead Generation logo" width="28" height="28"> Snapchat Lead Generation: Universal API

Create and manage Snapchat lead generation forms, webhook integrations, lead generation creatives, and lead generation ads through the Snapchat Marketing API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/snapchatLeadGeneration/latest
- **Category:** Marketing
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://forbusiness.snapchat.com
- **Vendor API docs:** https://developers.snap.com/api/marketing-api/Ads-API/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lead Generation Forms](actions/list-lead-generation-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/list-lead-generation-forms?connectionId=$CONNECTION_ID&adAccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Ad

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead Generation Ad](actions/create-lead-generation-ad.md) | POST | Creates a lead generation ad in Snapchat Lead Generation. |

### Creative

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead Generation Creative](actions/create-lead-generation-creative.md) | POST | Creates a lead generation creative in Snapchat Lead Generation. |

### Lead Generation Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead Generation Form](actions/create-lead-generation-form.md) | POST | Creates a lead generation form in Snapchat Lead Generation. |
| [Get Lead Generation Form](actions/get-lead-generation-form.md) | GET | Retrieves a lead generation form from Snapchat Lead Generation. |
| [List Lead Generation Forms](actions/list-lead-generation-forms.md) | GET | Retrieves lead generation forms from Snapchat Lead Generation. |

### Webhook Integration

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Integration](actions/create-webhook-integration.md) | POST | Creates a webhook integration in Snapchat Lead Generation. |
| [Delete Webhook Integration](actions/delete-webhook-integration.md) | DELETE | Deletes a webhook integration from Snapchat Lead Generation. |
| [List Webhook Integrations](actions/list-webhook-integrations.md) | GET | Retrieves webhook integrations for a form in Snapchat Lead Generation. |

### Webhook Test Event

| Action | Method | Description |
| --- | --- | --- |
| [Send Test Lead Data](actions/send-test-lead-data.md) | POST | Sends test lead data in Snapchat Lead Generation. |

