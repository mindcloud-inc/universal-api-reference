# VideoDB: Upload to Collection

Uploads media to a collection in VideoDB.

```
POST https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/upload-to-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VideoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/upload-to-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "default",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/upload-to-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "default",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Collection ID to upload into Default: `default`. |
| `url` | string | yes | Public media URL to ingest |
| `name` | string | no | Name for the uploaded media |
| `mediaType` | string | no | Media type such as video Default: `video`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | Optional callback URL |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "outputUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `outputUrl` | string |  |

## Native endpoint

Through the native VideoDB API, this operation is `POST /collection/:collection_id/upload` (base URL `https://api.videodb.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-to-collection.md) for the provider-specific parameters and requirements.

