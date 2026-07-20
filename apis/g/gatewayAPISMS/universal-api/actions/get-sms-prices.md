# GatewayAPI SMS: Get SMS Prices

Retrieves GatewayAPI SMS prices by country and prefix.

```
GET https://connect.mindcloud.co/v1/universal/gatewayAPISMS/latest/actions/get-sms-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatewayAPI SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatewayAPISMS/latest/actions/get-sms-prices?connectionId=$CONNECTION_ID&fileformat=json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileformat": "json"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatewayAPISMS/latest/actions/get-sms-prices?${params}`, {
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
| `fileformat` | string | yes | Output format for the SMS price list. Default: `json`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "premium": [
        {
          "country": "string",
          "dkk": 1,
          "eur": 1,
          "prefix": 1
        }
      ],
      "standard": [
        {
          "country": "string",
          "dkk": 1,
          "eur": 1,
          "prefix": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `premium[].country` | string |  |
| `premium[].dkk` | number |  |
| `premium[].eur` | number |  |
| `premium[].prefix` | number |  |
| `standard[].country` | string |  |
| `standard[].dkk` | number |  |
| `standard[].eur` | number |  |
| `standard[].prefix` | number |  |

## Native endpoint

Through the native GatewayAPI SMS API, this operation is `GET /api/prices/list/sms/:fileformat` (base URL `https://gatewayapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-prices.md) for the provider-specific parameters and requirements.

