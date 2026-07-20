# <img src="https://images.mindcloud.co/apps/icons/removebg_1773862957761.png" alt="Remove.bg logo" width="28" height="28"> Remove.bg: Universal API

Remove backgrounds, check credits, and submit improvement samples

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/removebg/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.remove.bg
- **Vendor API docs:** https://www.remove.bg/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/removebg/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account credit balances from Remove.bg. |

### Background Removal Result

| Action | Method | Description |
| --- | --- | --- |
| [Remove Background](actions/remove-background.md) | POST | Creates a background-removed image in Remove.bg. |

### Improvement Submission

| Action | Method | Description |
| --- | --- | --- |
| [Submit Improvement](actions/submit-improvement.md) | POST | Creates an improvement submission in Remove.bg. |

