# <img src="https://images.mindcloud.co/apps/icons/fraud-sentinel_1775673951546.png" alt="FraudSentinel logo" width="28" height="28"> FraudSentinel: Universal API

Monitor ad fraud and evaluate traffic IP risk

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fraudSentinel/latest
- **Category:** Marketing / Advertising
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fraudsentinel.com/
- **Vendor API docs:** https://www.clickfreeze.io/restapi

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get IP Risk](actions/get-ip-risk.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fraudSentinel/latest/actions/get-ip-risk?connectionId=$CONNECTION_ID&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Ip Address

| Action | Method | Description |
| --- | --- | --- |
| [Get IP Risk](actions/get-ip-risk.md) | GET |  |

