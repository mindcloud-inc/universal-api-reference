# Evervault: Retrieve Merchant

Retrieves a merchant from Evervault.

```
GET https://connect.mindcloud.co/v1/universal/evervault/latest/actions/retrieve-merchant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/retrieve-merchant?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evervault/latest/actions/retrieve-merchant?${params}`, {
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
      "applePay": {},
      "business": {},
      "categoryCode": "string",
      "createdAt": 1,
      "id": "string",
      "name": "Ava Chen",
      "networkTokens": {},
      "updatedAt": 1,
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applePay` | object |  |
| `business` | object |  |
| `categoryCode` | string |  |
| `createdAt` | number |  |
| `id` | string |  |
| `name` | string |  |
| `networkTokens` | object |  |
| `updatedAt` | number |  |
| `website` | string |  |

## Native endpoint

Through the native Evervault API, this operation is `GET /payments/merchants/{merchant_id}` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-merchant.md) for the provider-specific parameters and requirements.

