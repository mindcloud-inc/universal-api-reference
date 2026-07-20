# Zoho Books: Get Item



```
GET https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-item?connectionId=$CONNECTION_ID&itemId=1234567890&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "1234567890",
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-item?${params}`, {
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
| `itemId` | list<string> | yes | Unique identifier of the item. Example: `1234567890`. |
| `organizationId` | list<string> | yes | ID of the organization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "accountName": "Ava Chen",
      "createdTime": "string",
      "description": "string",
      "hasAttachment": true,
      "isTaxable": true,
      "itemId": "string",
      "itemType": "string",
      "lastModifiedTime": "string",
      "name": "Ava Chen",
      "productTaxCategory": {},
      "productType": "string",
      "purchaseRate": 1,
      "rate": 1,
      "sku": "string",
      "status": "string",
      "tags": [
        {}
      ],
      "unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Associated sales account ID. |
| `accountName` | string | Associated sales account name. |
| `createdTime` | string | Creation timestamp. |
| `description` | string | Item description. |
| `hasAttachment` | boolean | Whether the item has an attachment. |
| `isTaxable` | boolean | Whether the item is taxable. |
| `itemId` | string | Unique identifier of the item. |
| `itemType` | string | Type of the item. |
| `lastModifiedTime` | string | Last modification timestamp. |
| `name` | string | Item name. |
| `productTaxCategory` | object | Product tax category details. |
| `productType` | string | Product classification of the item. |
| `purchaseRate` | number | Purchase rate of the item. |
| `rate` | number | Sales rate of the item. |
| `sku` | string | Stock keeping unit. |
| `status` | string | Item status. |
| `tags` | array<object> | Tags associated with the item. |
| `unit` | string | Measurement unit for the item. |

## Native endpoint

Through the native Zoho Books API, this operation is `GET /items/:item_id` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

