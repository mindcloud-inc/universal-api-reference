# Evervault: Card Insights

Retrieves payment card insights from Evervault.

```
GET https://connect.mindcloud.co/v1/universal/evervault/latest/actions/card-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/card-insights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evervault/latest/actions/card-insights?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "bin": {},
      "capabilities": {},
      "cardholder": {},
      "createdAt": 1,
      "cvv": {},
      "fees": {},
      "fingerprint": "string",
      "id": "string",
      "paymentAccountReference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `bin` | object |  |
| `capabilities` | object |  |
| `cardholder` | object |  |
| `createdAt` | number |  |
| `cvv` | object |  |
| `fees` | object |  |
| `fingerprint` | string |  |
| `id` | string |  |
| `paymentAccountReference` | string |  |

## Native endpoint

Through the native Evervault API, this operation is `POST /insights/cards` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/card-insights.md) for the provider-specific parameters and requirements.

