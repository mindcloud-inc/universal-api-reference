# SureCart: List Purchases



```
GET https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-purchases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-purchases?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-purchases?${params}`, {
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

Through the native SureCart API, this operation is `GET v1/purchases` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-purchases.md) for the provider-specific parameters and requirements.

