# Printful: Delete Store Product

Deletes a sync product from a Printful store.

```
DELETE https://connect.mindcloud.co/v1/universal/printful/latest/actions/delete-store-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/printful/latest/actions/delete-store-product?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printful/latest/actions/delete-store-product?${params}`, {
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
| `id` | string | yes | The Printful sync product id. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "external_id": "string",
      "id": 1,
      "name": "Ava Chen",
      "thumbnail_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `external_id` | string |  |
| `id` | number |  |
| `name` | string |  |
| `thumbnail_url` | string |  |

## Native endpoint

Through the native Printful API, this operation is `DELETE /store/products/{id}` (base URL `https://api.printful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-store-product.md) for the provider-specific parameters and requirements.

