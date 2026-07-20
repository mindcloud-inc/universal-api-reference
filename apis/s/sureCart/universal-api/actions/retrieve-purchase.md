# SureCart: Retrieve Purchase



```
GET https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-purchase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-purchase?connectionId=$CONNECTION_ID&id=bf93f41e-bd59-4540-a9c1-f1f3b4f5bf8d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "bf93f41e-bd59-4540-a9c1-f1f3b4f5bf8d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-purchase?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The purchase ID to retrieve. Example: `bf93f41e-bd59-4540-a9c1-f1f3b4f5bf8d`. |

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

Through the native SureCart API, this operation is `GET v1/purchases/:id` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-purchase.md) for the provider-specific parameters and requirements.

