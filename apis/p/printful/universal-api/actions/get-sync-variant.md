# Printful: Get Sync Variant

Retrieves a synced variant from your Printful integrations.

```
GET https://connect.mindcloud.co/v1/universal/printful/latest/actions/get-sync-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printful/latest/actions/get-sync-variant?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printful/latest/actions/get-sync-variant?${params}`, {
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
| `id` | string | yes | The Printful ecommerce platform sync variant id. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "external_id": "string",
      "id": 1,
      "name": "Ava Chen",
      "sku": "string"
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
| `sku` | string |  |

## Native endpoint

Through the native Printful API, this operation is `GET /sync/variant/{id}` (base URL `https://api.printful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sync-variant.md) for the provider-specific parameters and requirements.

