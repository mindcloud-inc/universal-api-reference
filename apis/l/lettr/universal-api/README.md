# <img src="https://images.mindcloud.co/apps/icons/lettr-icon_1775679282830.png" alt="Lettr logo" width="28" height="28"> Lettr: Universal API

Send transactional and scheduled emails, manage domains, templates, and webhooks with the Lettr REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lettr/latest
- **Category:** Communication / Email Communications
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lettr.com
- **Vendor API docs:** https://docs.lettr.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Auth Check](actions/auth-check.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/auth-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | POST |  |
| [Delete Domain](actions/delete-domain.md) | DELETE |  |
| [Get Domain](actions/get-domain.md) | GET |  |
| [List Domains](actions/list-domains.md) | GET |  |
| [Verify Domain](actions/verify-domain.md) | PUT |  |

### Email Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST |  |
| [Delete Template](actions/delete-template.md) | DELETE |  |
| [Get Template](actions/get-template.md) | GET |  |
| [Get Template Merge Tags](actions/get-template-merge-tags.md) | GET |  |
| [Get Template Merge Tags By Version](actions/get-template-merge-tags-by-version.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |
| [Update Template](actions/update-template.md) | PUT |  |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Detail](actions/get-email-detail.md) | GET |  |
| [Send Email](actions/send-email.md) | POST |  |
| [Send HTML Email](actions/send-html-email.md) | POST |  |
| [Send Template Email](actions/send-template-email.md) | POST |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Bounce Events](actions/list-bounce-events.md) | GET |  |
| [List Delivery Events](actions/list-delivery-events.md) | GET |  |
| [List Email Events](actions/list-email-events.md) | GET |  |
| [List Email Events For Transmission](actions/list-email-events-for-transmission.md) | GET |  |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Scheduled Email](actions/cancel-scheduled-email.md) | DELETE |  |
| [Get Scheduled Email](actions/get-scheduled-email.md) | GET |  |
| [Schedule Email](actions/schedule-email.md) | POST |  |
| [Schedule HTML Email](actions/schedule-html-email.md) | POST |  |
| [Schedule Template Email](actions/schedule-template-email.md) | POST |  |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Auth Check](actions/auth-check.md) | GET |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

