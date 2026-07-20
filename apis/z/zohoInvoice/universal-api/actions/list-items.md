# Zoho Invoice: List Items

Retrieves items from Zoho Invoice.

```
GET https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-items?${params}`, {
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
| `searchText` | string | no | Example: `support`. |
| `name` | string | no | Example: `Premium Support`. |
| `description` | string | no | Example: `Monthly support`. |
| `rate` | string | no | Example: `100`. |
| `taxId` | string | no | Example: `903000000012345`. |
| `filterBy` | list<string> | no | One of: `Status.Active`, `Status.All`, `Status.Inactive`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nameStartswith` | string | no | Example: `Prem`. |
| `nameContains` | string | no | Example: `Support`. |
| `descriptionStartswith` | string | no | Example: `Monthly`. |
| `descriptionContains` | string | no | Example: `support`. |
| `rateLessThan` | string | no | Example: `100`. |
| `rateLessEquals` | string | no | Example: `100`. |
| `rateGreaterThan` | string | no | Example: `100`. |
| `rateGreaterEquals` | string | no | Example: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "hasAttachment": true,
      "itemId": "string",
      "itemName": "Ava Chen",
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "productType": "string",
      "rate": 1,
      "sku": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date |  |
| `description` | string |  |
| `hasAttachment` | boolean |  |
| `itemId` | string |  |
| `itemName` | string |  |
| `lastModifiedTime` | date |  |
| `name` | string |  |
| `productType` | string |  |
| `rate` | number |  |
| `sku` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Invoice API, this operation is `GET /items` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

