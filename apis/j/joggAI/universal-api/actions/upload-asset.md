# JoggAI: Upload Asset



```
POST https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/upload-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/upload-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contentType": "string",
  "filename": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/upload-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contentType": "string",
    "filename": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentType` | string | yes | MIME type of the file |
| `filename` | string | yes | Name of the file to upload |
| `fileSize` | number | no | File size in bytes |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assetUrl": "https://example.com",
      "signUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetUrl` | string | Reusable asset URL to reference in later JoggAI requests |
| `signUrl` | string | Signed upload URL for the file PUT step |

## Native endpoint

Through the native JoggAI API, this operation is `POST /v2/upload/asset` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-asset.md) for the provider-specific parameters and requirements.

