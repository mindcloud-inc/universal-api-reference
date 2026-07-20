# Corporate Merch: Update Order Address

Updates an order address in Corporate Merch.

```
PUT https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/update-order-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Corporate Merch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/update-order-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/update-order-address', {
  method: 'PUT',
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
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Corporate Merch API, this operation is `PUT /v2/orders/{id}/update_address` (base URL `https://api.corporatemerch.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order-address.md) for the provider-specific parameters and requirements.

