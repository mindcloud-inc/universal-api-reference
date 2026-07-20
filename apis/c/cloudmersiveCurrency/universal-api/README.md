# <img src="https://images.mindcloud.co/apps/icons/cloudmersive-icon_1777994515710.png" alt="Cloudmersive Currency logo" width="28" height="28"> Cloudmersive Currency: Universal API

Retrieve Cloudmersive currency exchange rates, list supported currencies, and convert prices between currency pairs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudmersiveCurrency/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloudmersive.com/currency-api
- **Vendor API docs:** https://api.cloudmersive.com/docs/currency.asp

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Available Currencies](actions/list-available-currencies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveCurrency/latest/actions/list-available-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Available Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Available Currencies](actions/list-available-currencies.md) | GET | Retrieves available currencies from Cloudmersive Currency. |

### Converted Currency Result

| Action | Method | Description |
| --- | --- | --- |
| [Convert Currency](actions/convert-currency.md) | GET | Converts a currency amount in Cloudmersive Currency. |

### Exchange Rate Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Exchange Rate](actions/get-exchange-rate.md) | GET | Retrieves an exchange rate from Cloudmersive Currency. |

