# MoySklad: Create product

Creates a product in MoySklad.

```
POST https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Validator Product"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Validator Product"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Product name. Required by MoySklad for product creation. Default: `MindCloud Validator Product`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "archived": true,
      "code": "string",
      "externalCode": "string",
      "group": {},
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "owner": {},
      "shared": true,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | MoySklad account identifier. |
| `archived` | boolean | Whether the product is archived. |
| `code` | string | Product code. |
| `externalCode` | string | External code. |
| `group` | object | Group metadata. |
| `id` | string | Product identifier. |
| `meta` | object | MoySklad entity metadata including href, type, and mediaType. |
| `name` | string | Product name. |
| `owner` | object | Owner metadata. |
| `shared` | boolean | Whether the product is shared. |
| `updated` | date | Last updated timestamp. |

## Native endpoint

Through the native MoySklad API, this operation is `POST entity/product` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

