# <img src="https://images.mindcloud.co/apps/icons/encodian_1777473729909.jpeg" alt="Encodian - Sign logo" width="28" height="28"> Encodian - Sign: Universal API

Send documents for signature using Encodian Sign.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/encodianSign/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.encodian.com/product/sign/
- **Vendor API docs:** https://support.encodian.com/hc/en-gb/sections/25624905449116-Power-Automate-Action-Documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Trigr Subscription Status](actions/get-trigr-subscription-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/get-trigr-subscription-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Envelope

| Action | Method | Description |
| --- | --- | --- |
| [Sign - Send File For Signature](actions/sign-send-file-for-signature.md) | POST |  |

### Trigr Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Trigr Subscription Status](actions/get-trigr-subscription-status.md) | GET |  |

### Trigr Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Trigr Webhook Subscription](actions/create-trigr-webhook-subscription.md) | POST |  |
| [Delete Trigr Webhook Subscription](actions/delete-trigr-webhook-subscription.md) | DELETE |  |

