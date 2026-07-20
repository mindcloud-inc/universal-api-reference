# OPN: Get Transaction

Retrieves details for a transaction from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-transaction?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-transaction?${params}`, {
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
      "amount": 1,
      "created_at": "string",
      "currency": "string",
      "direction": "string",
      "id": "string",
      "key": "string",
      "livemode": true,
      "location": "string",
      "merchant_name": "Ava Chen",
      "merchant_uid": "string",
      "object": "string",
      "origin": "string",
      "transferable_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `created_at` | string |  |
| `currency` | string |  |
| `direction` | string |  |
| `id` | string |  |
| `key` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `merchant_name` | string |  |
| `merchant_uid` | string |  |
| `object` | string |  |
| `origin` | string |  |
| `transferable_at` | string |  |

## Native endpoint

Through the native OPN API, this operation is `GET /transactions/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

