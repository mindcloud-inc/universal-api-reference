# Gemini: Upload File Media

Uploads a file to Gemini.

```
POST https://connect.mindcloud.co/v1/universal/gemini/latest/actions/upload-file-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/upload-file-media" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gemini/latest/actions/upload-file-media', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | object | yes | File metadata object for upload initialization. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": "2026-05-07T12:00:00.000Z",
      "expirationTime": "2026-05-07T12:00:00.000Z",
      "mimeType": "string",
      "name": "Ava Chen",
      "sizeBytes": 1,
      "source": "string",
      "state": "string",
      "updateTime": "2026-05-07T12:00:00.000Z",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | date | Creation timestamp. |
| `expirationTime` | date | Expiration timestamp. |
| `mimeType` | string | MIME type of the file. |
| `name` | string | File resource name. |
| `sizeBytes` | number | File size in bytes. |
| `source` | string | File source classification. |
| `state` | string | File processing state. |
| `updateTime` | date | Last update timestamp. |
| `uri` | string | File URI. |

## Native endpoint

Through the native Gemini API, this operation is `POST v1beta/files` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-media.md) for the provider-specific parameters and requirements.

