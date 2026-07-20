# ProdPad: List Products

Retrieves products from ProdPad.

```
GET https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProdPad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-products?${params}`, {
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
| `group` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "documentation": "string",
      "id": 1,
      "image": {
        "original": "string"
      },
      "kpis": "string",
      "name": "Ava Chen",
      "roadmaps": {
        "id": "string"
      },
      "updated_at": "2026-05-07T12:00:00.000Z",
      "value": "string",
      "vision": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `description` | string |  |
| `documentation` | string |  |
| `id` | number |  |
| `image.original` | string |  |
| `kpis` | string |  |
| `name` | string |  |
| `roadmaps.id` | string |  |
| `updated_at` | date |  |
| `value` | string |  |
| `vision` | string |  |

## Native endpoint

Through the native ProdPad API, this operation is `GET /products` (base URL `https://api.prodpad.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

