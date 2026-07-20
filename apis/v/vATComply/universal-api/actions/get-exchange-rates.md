# VAT Comply: Get Exchange Rates

Retrieves exchange rates from VAT Comply.

```
GET https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/get-exchange-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VAT Comply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/get-exchange-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/get-exchange-rates?${params}`, {
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
| `base` | string | no | Base currency for the rates response. Default: `EUR`. |
| `symbols` | string | no | Comma-separated target currency symbols. |
| `date` | string | no | Historical date for the requested exchange rates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base": "string",
      "date": "string",
      "rates": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base` | string |  |
| `date` | string |  |
| `rates` | object |  |

## Native endpoint

Through the native VAT Comply API, this operation is `GET /rates` (base URL `https://api.vatcomply.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-exchange-rates.md) for the provider-specific parameters and requirements.

