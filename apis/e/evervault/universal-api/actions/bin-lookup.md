# Evervault: BIN Lookup

Retrieves BIN lookup details from Evervault.

```
GET https://connect.mindcloud.co/v1/universal/evervault/latest/actions/bin-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/bin-lookup?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evervault/latest/actions/bin-lookup?${params}`, {
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
      "brand": "string",
      "country": "string",
      "createdAt": 1,
      "currency": "string",
      "fastFunds": {},
      "funding": "string",
      "id": "string",
      "issuer": "string",
      "productName": "Ava Chen",
      "segment": "string",
      "threeDS": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | string |  |
| `country` | string |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `fastFunds` | object |  |
| `funding` | string |  |
| `id` | string |  |
| `issuer` | string |  |
| `productName` | string |  |
| `segment` | string |  |
| `threeDS` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Evervault API, this operation is `POST /payments/bin-lookups` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bin-lookup.md) for the provider-specific parameters and requirements.

