# Alto: Get Inventory Landlords

Retrieves landlords for an inventory item in Alto.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory-landlords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory-landlords?connectionId=$CONNECTION_ID&inventoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inventoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory-landlords?${params}`, {
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
      "createdDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "forename": "Ava Chen",
      "id": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "phone": "string",
      "surname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | date |  |
| `email` | string |  |
| `forename` | string |  |
| `id` | string |  |
| `modifiedDate` | date |  |
| `phone` | string |  |
| `surname` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /inventory/:inventoryId/landlords` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory-landlords.md) for the provider-specific parameters and requirements.

