# <img src="https://images.mindcloud.co/apps/icons/caller-api_1774987447992.png" alt="CallerAPI logo" width="28" height="28"> CallerAPI: Universal API

Look up phone reputation, porting, identity, and spam reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/callerAPI/latest
- **Category:** Marketing
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://callerapi.com
- **Vendor API docs:** https://docs.callerapi.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance and Email](actions/get-balance-and-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callerAPI/latest/actions/get-balance-and-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance and Email](actions/get-balance-and-email.md) | GET | Retrieves account balance and email from CallerAPI. |

### Phone Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Spam Score and HLR](actions/lookup-spam-score-and-hlr.md) | GET | Retrieves spam score and HLR data from CallerAPI. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves webhook subscriptions from CallerAPI. |

