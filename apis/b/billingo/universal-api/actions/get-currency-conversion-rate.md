# Billingo: Get Currency Conversion Rate

Retrieves currency conversion rates from Billingo.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-currency-conversion-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-currency-conversion-rate?connectionId=$CONNECTION_ID&from=HUF&to=EUR" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "HUF",
  "to": "EUR"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-currency-conversion-rate?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | Source currency code for the conversion rate. Default: `HUF`. Example: `HUF`. |
| `to` | string | yes | Target currency code for the conversion rate. Default: `EUR`. Example: `EUR`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | date | no | Optional conversion-rate date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversation_rate": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "from_currency": "string",
      "to_currency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversation_rate` | number |  |
| `date` | date |  |
| `from_currency` | string |  |
| `to_currency` | string |  |

## Native endpoint

Through the native Billingo API, this operation is `GET /currencies` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-currency-conversion-rate.md) for the provider-specific parameters and requirements.

