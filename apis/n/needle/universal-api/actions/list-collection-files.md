# Needle: List Collection Files

Retrieves files from a Needle collection.

```
GET https://connect.mindcloud.co/v1/universal/needle/latest/actions/list-collection-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Needle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/needle/latest/actions/list-collection-files?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/needle/latest/actions/list-collection-files?${params}`, {
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
| `collectionId` | string | yes | ID of the collection whose files will be listed |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connectorId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "md5Hash": "string",
      "name": "Ava Chen",
      "size": 1,
      "status": "string",
      "type": "string",
      "url": "https://example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectorId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `md5Hash` | string |  |
| `name` | string |  |
| `size` | number |  |
| `status` | string |  |
| `type` | string |  |
| `url` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Needle API, this operation is `GET /api/v1/collections/:collectionId/files` (base URL `https://needle.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-collection-files.md) for the provider-specific parameters and requirements.

