# <img src="https://images.mindcloud.co/apps/icons/wafrow_1775769313016.png" alt="Wafrow logo" width="28" height="28"> Wafrow: Universal API

Generate personalized campaign images, email creatives, and dynamic visual variants from Wafrow templates.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wafrow/latest
- **Category:** Marketing
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wafrow.com/
- **Vendor API docs:** https://wafrow.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wafrow/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Save Variant](actions/save-variant.md) | POST | Creates a saved personalization variant in Wafrow. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get Variant Image](actions/get-variant-image.md) | GET | Retrieves a rendered variant image from Wafrow. |
| [Pre-render Image](actions/pre-render-image.md) | POST | Creates a pre-rendered image or PDF in Wafrow. |
| [Pre-render Image From Webhook](actions/pre-render-image-from-webhook.md) | POST | Creates a pre-rendered image or PDF in Wafrow from webhook input. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves current user details from Wafrow. |

