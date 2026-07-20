# Zoho Books: List Items



```
GET https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-items?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-items?${params}`, {
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
| `organizationId` | list<string> | yes | ID of the organization. |
| `name` | string | no | Search items by name. Example: `Hard Drive`. |
| `description` | string | no | Search items by description. Example: `500GB`. |
| `rate` | number | no | Search items by rate. Example: `120`. |
| `filterBy` | list<string> | no | Filter items by status bucket. One of: `Status.Active`, `Status.All`, `Status.Inactive`. |
| `searchText` | string | no | Search items by name or description. Example: `Drive`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taxId` | string | no | Search items by tax ID. Example: `1234567890`. |
| `taxName` | string | no | Search items by tax name. Example: `Sales Tax`. |
| `isTaxable` | boolean | no | Filter by taxable status. |
| `taxExemptionId` | string | no | Tax exemption ID when filtering non-taxable items. Example: `1234567890`. |
| `accountId` | string | no | Filter by linked account ID. Example: `1234567890`. |
| `satItemKeyCode` | string | no | SAT item key code filter. Example: `71121206`. |
| `unitkeyCode` | string | no | SAT unit code filter. Example: `E48`. |

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

Through the native Zoho Books API, this operation is `GET /items` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

