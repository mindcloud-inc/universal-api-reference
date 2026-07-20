# Alto: Get Inventory Item

Retrieves an inventory item from Alto by ID.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory-item?connectionId=$CONNECTION_ID&inventoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inventoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory-item?${params}`, {
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
| `inventoryId` | string | yes | Unique Alto inventory item identifier. |

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

Through the native Alto API, this operation is `GET /inventory/:inventoryId` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory-item.md) for the provider-specific parameters and requirements.

