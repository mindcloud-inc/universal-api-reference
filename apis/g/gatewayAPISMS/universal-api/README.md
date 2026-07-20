# <img src="https://images.mindcloud.co/apps/icons/gateway-api-sms_1782742987991.png" alt="GatewayAPI SMS logo" width="28" height="28"> GatewayAPI SMS: Universal API

Send and track SMS messages with GatewayAPI

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gatewayAPISMS/latest
- **Category:** Communication / Team Messaging
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gatewayapi.com
- **Vendor API docs:** https://gatewayapi.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Balance](actions/get-account-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatewayAPISMS/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Account Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET | Retrieves your GatewayAPI SMS account balance and currency. |

### Keyword

| Action | Method | Description |
| --- | --- | --- |
| [List Keywords](actions/list-keywords.md) | GET | Retrieves configured keywords from GatewayAPI SMS. |

### Keyword Availability

| Action | Method | Description |
| --- | --- | --- |
| [Check Keyword Availability](actions/check-keyword-availability.md) | GET | Checks whether a keyword is available in GatewayAPI SMS. |

### Label Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage by Label](actions/get-usage-by-label.md) | GET | Retrieves GatewayAPI SMS usage by label and country. |

### Sms Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Prices](actions/get-sms-prices.md) | GET | Retrieves GatewayAPI SMS prices by country and prefix. |

