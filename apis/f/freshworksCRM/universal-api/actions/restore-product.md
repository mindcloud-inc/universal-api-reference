# Freshworks CRM: Restore Product

Restores a product in Freshworks CRM.

```
PUT https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/restore-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/restore-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/restore-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "product": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "creater_id": 1,
        "description": "string",
        "id": 1,
        "is_active": true,
        "is_deleted": true,
        "name": "Ava Chen",
        "owner_id": 1,
        "pricing_type": 1,
        "updated_at": "2026-05-07T12:00:00.000Z",
        "updater_id": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `product.created_at` | date |  |
| `product.creater_id` | number |  |
| `product.description` | string |  |
| `product.id` | number |  |
| `product.is_active` | boolean |  |
| `product.is_deleted` | boolean |  |
| `product.name` | string |  |
| `product.owner_id` | number |  |
| `product.pricing_type` | number |  |
| `product.updated_at` | date |  |
| `product.updater_id` | number |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `PUT /api/cpq/products/:id/restore` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-product.md) for the provider-specific parameters and requirements.

