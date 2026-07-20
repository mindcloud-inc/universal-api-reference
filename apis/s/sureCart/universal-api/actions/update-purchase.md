# SureCart: Update Purchase



```
PUT https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/update-purchase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/update-purchase" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "bf93f41e-bd59-4540-a9c1-f1f3b4f5bf8d",
  "purchase.revokeAt": "2026-04-05 00:00:00 UTC"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/update-purchase', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "bf93f41e-bd59-4540-a9c1-f1f3b4f5bf8d",
    "purchase.revokeAt": "2026-04-05 00:00:00 UTC"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The purchase ID to update. Example: `bf93f41e-bd59-4540-a9c1-f1f3b4f5bf8d`. |
| `purchase.revokeAt` | string | yes | When the purchase should be revoked, for example 2026-04-05 00:00:00 UTC. Example: `2026-04-05 00:00:00 UTC`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "customer": "string",
      "id": "string",
      "initialOrder": "string",
      "license": "string",
      "liveMode": true,
      "object": "string",
      "price": "string",
      "product": "string",
      "quantity": 1,
      "review": "string",
      "revokeAt": 1,
      "revoked": true,
      "revokedAt": 1,
      "subscription": "string",
      "updatedAt": 1,
      "variant": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `customer` | string |  |
| `id` | string |  |
| `initialOrder` | string |  |
| `license` | string |  |
| `liveMode` | boolean |  |
| `object` | string |  |
| `price` | string |  |
| `product` | string |  |
| `quantity` | number |  |
| `review` | string |  |
| `revokeAt` | number |  |
| `revoked` | boolean |  |
| `revokedAt` | number |  |
| `subscription` | string |  |
| `updatedAt` | number |  |
| `variant` | string |  |

## Native endpoint

Through the native SureCart API, this operation is `PATCH v1/purchases/:id` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-purchase.md) for the provider-specific parameters and requirements.

