# Orshot: Upload Brand Asset Image



```
POST https://connect.mindcloud.co/v1/universal/orshot/latest/actions/upload-brand-asset-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orshot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/upload-brand-asset-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orshot/latest/actions/upload-brand-asset-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | yes | Image URL or base64-encoded image string. |
| `fileName` | string | no | Optional filename for the uploaded image. |
| `fileType` | string | no | Optional MIME type for the uploaded image. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "asset": {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "directUrl": "https://example.com",
          "fileName": "Ava Chen",
          "fileSize": 1,
          "id": 1,
          "meta": {},
          "tags": [
            "string"
          ],
          "userId": "string",
          "workspaceId": 1
        },
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.asset.createdAt` | date | Timestamp when the image asset was created. |
| `data.asset.directUrl` | string | Stored direct URL for the uploaded image asset. |
| `data.asset.fileName` | string | Stored filename for the uploaded image asset. |
| `data.asset.fileSize` | number | Image asset file size in bytes. |
| `data.asset.id` | number | Uploaded image asset identifier. |
| `data.asset.meta` | object | Provider metadata returned for the uploaded image asset. |
| `data.asset.tags` | array<string> | Tags associated with the uploaded image asset. |
| `data.asset.userId` | string | User that created the uploaded image asset. |
| `data.asset.workspaceId` | number | Workspace that owns the uploaded image asset. |
| `data.url` | string | Convenience direct URL for the uploaded image asset. |

## Native endpoint

Through the native Orshot API, this operation is `POST /brand-assets/images/add` (base URL `https://api.orshot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-brand-asset-image.md) for the provider-specific parameters and requirements.

