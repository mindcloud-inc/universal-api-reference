# TrackMage: Get Product

Retrieves a product from your TrackMage account.

```
GET https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-product?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-product?${params}`, {
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
| `id` | string | yes | Resource identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalSourceIntegration": "string",
      "externalSourceSyncId": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "name": "Ava Chen",
      "originUrl": "https://example.com",
      "productVariants": [
        "string"
      ],
      "sku": "string",
      "team": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalSourceIntegration` | string |  |
| `externalSourceSyncId` | string |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `name` | string |  |
| `originUrl` | string |  |
| `productVariants` | array<string> |  |
| `sku` | string |  |
| `team` | string |  |

## Native endpoint

Through the native TrackMage API, this operation is `GET /products/{id}` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

