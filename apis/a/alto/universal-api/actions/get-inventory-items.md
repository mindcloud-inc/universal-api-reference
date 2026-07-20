# Alto: Get Inventory Items

Retrieves inventory items from Alto by IDs.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory-items?connectionId=$CONNECTION_ID&inventoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inventoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory-items?${params}`, {
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
| `inventoryId` | string | yes | Inventory item identifier to retrieve. The endpoint accepts one or more inventory IDs. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bathrooms": 1,
      "bedrooms": 1,
      "branchId": "string",
      "category": "string",
      "id": "string",
      "price": 1,
      "recordType": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bathrooms` | number |  |
| `bedrooms` | number |  |
| `branchId` | string |  |
| `category` | string |  |
| `id` | string |  |
| `price` | number |  |
| `recordType` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /inventory/items` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory-items.md) for the provider-specific parameters and requirements.

