# OPN: Get Capability

Retrieves account capability details from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-capability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-capability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-capability?${params}`, {
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
      "banks": [
        "string"
      ],
      "country": "string",
      "limits": {},
      "location": "string",
      "object": "string",
      "payment_methods": [
        {}
      ],
      "tokenization_methods": [
        "string"
      ],
      "zero_interest_installments": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `banks` | array<string> |  |
| `country` | string |  |
| `limits` | object |  |
| `location` | string |  |
| `object` | string |  |
| `payment_methods` | array<object> |  |
| `tokenization_methods` | array<string> |  |
| `zero_interest_installments` | boolean |  |

## Native endpoint

Through the native OPN API, this operation is `GET /capability` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-capability.md) for the provider-specific parameters and requirements.

