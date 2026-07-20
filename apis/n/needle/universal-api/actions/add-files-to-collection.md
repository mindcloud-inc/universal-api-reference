# Needle: Add Files To Collection

Adds files to a collection in Needle.

```
POST https://connect.mindcloud.co/v1/universal/needle/latest/actions/add-files-to-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Needle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/needle/latest/actions/add-files-to-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "files[].name": "Ava Chen",
  "files[].url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/needle/latest/actions/add-files-to-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "files[].name": "Ava Chen",
    "files[].url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | ID of the collection to add files to |
| `files[].name` | string | yes | Display name of the file to add |
| `files[].url` | string | yes | URL of the file to add to the collection |

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

Through the native Needle API, this operation is `POST /api/v1/collections/:collectionId/files` (base URL `https://needle.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-files-to-collection.md) for the provider-specific parameters and requirements.

