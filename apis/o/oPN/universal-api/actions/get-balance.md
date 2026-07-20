# OPN: Get Balance

Retrieves account balance details from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-balance?${params}`, {
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
      "at": "string",
      "created_at": "string",
      "currency": "string",
      "livemode": true,
      "location": "string",
      "object": "string",
      "on_hold": 1,
      "reserve": 1,
      "total": 1,
      "transferable": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `at` | string |  |
| `created_at` | string |  |
| `currency` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `object` | string |  |
| `on_hold` | number |  |
| `reserve` | number |  |
| `total` | number |  |
| `transferable` | number |  |

## Native endpoint

Through the native OPN API, this operation is `GET /balance` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-balance.md) for the provider-specific parameters and requirements.

