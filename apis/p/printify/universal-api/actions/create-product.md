# Printify: Create Product

Creates a product in Printify.

```
POST https://connect.mindcloud.co/v1/universal/printify/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printify/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blueprint_id": "5",
  "description": "MindCloud validator test product created by Codex.",
  "print_areas": {},
  "print_provider_id": "42",
  "shop_id": "27141936",
  "title": "MindCloud Printify Test Tee",
  "variants": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printify/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blueprint_id": "5",
    "description": "MindCloud validator test product created by Codex.",
    "print_areas": {},
    "print_provider_id": "42",
    "shop_id": "27141936",
    "title": "MindCloud Printify Test Tee",
    "variants": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blueprint_id` | number | yes | Blueprint id to create from. Default: `5`. |
| `description` | string | yes | Product description. Default: `MindCloud validator test product created by Codex.`. |
| `print_areas` | list<object> | yes | Print area configuration with uploaded artwork. |
| `print_provider_id` | number | yes | Print provider id to create from. Default: `42`. |
| `shop_id` | number | yes | Printify shop id. Default: `27141936`. |
| `title` | string | yes | Product title. Default: `MindCloud Printify Test Tee`. |
| `variants` | list<object> | yes | Enabled variants with prices. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blueprintId": 1,
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "isLocked": true,
      "printProviderId": 1,
      "shopId": 1,
      "title": "string",
      "updatedAt": "string",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blueprintId` | number |  |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `printProviderId` | number |  |
| `shopId` | number |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `visible` | boolean |  |

## Native endpoint

Through the native Printify API, this operation is `POST /shops/:shop_id/products.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

