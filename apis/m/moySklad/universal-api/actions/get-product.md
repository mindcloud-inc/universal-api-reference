# MoySklad: Get product

Retrieves the product from MoySklad.

```
GET https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-product?connectionId=$CONNECTION_ID&id=89e05606-3ce8-11f1-0a80-161100021282" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "89e05606-3ce8-11f1-0a80-161100021282"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-product?${params}`, {
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
| `id` | string | yes | MoySklad product id. Default: `89e05606-3ce8-11f1-0a80-161100021282`. |

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

Through the native MoySklad API, this operation is `GET entity/product/:id` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

