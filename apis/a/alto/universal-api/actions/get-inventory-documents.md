# Alto: Get Inventory Documents

Retrieves documents for an inventory item in Alto.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory-documents?connectionId=$CONNECTION_ID&limit=25&offset=0&inventoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "inventoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory-documents?${params}`, {
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
      "caption": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "fileName": "Ava Chen",
      "fileType": "string",
      "id": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caption` | string |  |
| `createdDate` | date |  |
| `fileName` | string |  |
| `fileType` | string |  |
| `id` | string |  |
| `modifiedDate` | date |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /inventory/:inventoryId/documents` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-inventory-documents.md) for the provider-specific parameters and requirements.

