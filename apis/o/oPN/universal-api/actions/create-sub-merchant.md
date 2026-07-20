# OPN: Create Sub Merchant

Creates a new sub Merchant in OPN.

```
POST https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-sub-merchant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-sub-merchant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-sub-merchant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "default_mid": "string",
      "id": "string",
      "level": 1,
      "live_account_status": "string",
      "name": "Ava Chen",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `default_mid` | string |  |
| `id` | string |  |
| `level` | number |  |
| `live_account_status` | string |  |
| `name` | string |  |
| `object` | string |  |

## Native endpoint

Through the native OPN API, this operation is `POST /sub_merchants` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sub-merchant.md) for the provider-specific parameters and requirements.

