# <img src="https://images.mindcloud.co/apps/icons/renderly_1775843397223.jpeg" alt="Renderly logo" width="28" height="28"> Renderly: Universal API

Create videos, manage templates, upload media, and track renders

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/renderly/latest
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://renderly.video
- **Vendor API docs:** https://renderly.video/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify API Key](actions/verify-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/renderly/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details and credits from Renderly. |
| [Verify API Key](actions/verify-api-key.md) | GET | Verifies an API key in Renderly. |

### Render Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Render Job](actions/create-render-job.md) | POST | Creates a video render job in Renderly. |
| [Get Render Status](actions/get-render-status.md) | GET | Retrieves a render job's status from Renderly. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves available video templates from Renderly. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Upload Media](actions/upload-media.md) | POST | Creates a media upload URL in Renderly. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook endpoint in Renderly. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook endpoint from Renderly. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves registered webhook endpoints from Renderly. |

