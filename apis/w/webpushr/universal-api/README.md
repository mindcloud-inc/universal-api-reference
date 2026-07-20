# <img src="https://images.mindcloud.co/apps/icons/webpushr_1774640993041.png" alt="Webpushr logo" width="28" height="28"> Webpushr: Universal API

Send, segment, and track website push notifications

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webpushr/latest
- **Category:** Marketing
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.webpushr.com
- **Vendor API docs:** https://www.webpushr.com/docs/introduction-to-rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Subscriber Count](actions/get-subscriber-count.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/get-subscriber-count?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Push Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Send Push to All Subscribers](actions/send-push-to-all-subscribers.md) | POST |  |
| [Send Push to Custom Attributes](actions/send-push-to-custom-attributes.md) | POST |  |
| [Send Push to Segments](actions/send-push-to-segments.md) | POST |  |
| [Send Push to Subscriber ID](actions/send-push-to-subscriber-id.md) | POST |  |

### Push Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Push Status](actions/get-push-status.md) | GET |  |

### Subscriber Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscriber Count](actions/get-subscriber-count.md) | GET |  |

