# Zoho Invoice: Get Item

Retrieves an item from Zoho Invoice.

```
GET https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/get-item?connectionId=$CONNECTION_ID&itemId=903000000045027" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "903000000045027"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/get-item?${params}`, {
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
| `itemId` | string | yes | Unique identifier of the item. Example: `903000000045027`. |

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

Through the native Zoho Invoice API, this operation is `GET /items/:item_id` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

