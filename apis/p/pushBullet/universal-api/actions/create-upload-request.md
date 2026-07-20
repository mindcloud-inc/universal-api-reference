# Pushbullet: Create Upload Request

Creates a file upload request in Pushbullet.

```
POST https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-upload-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-upload-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file_name": "Ava Chen",
  "file_type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-upload-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file_name": "Ava Chen",
    "file_type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file_name` | string | yes | Name of file to upload. |
| `file_type` | string | yes | MIME type of file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "fileName": "Ava Chen",
      "fileType": "string",
      "fileUrl": "https://example.com",
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `fileName` | string |  |
| `fileType` | string |  |
| `fileUrl` | string |  |
| `uploadUrl` | string |  |

## Native endpoint

Through the native Pushbullet API, this operation is `POST /upload-request` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-upload-request.md) for the provider-specific parameters and requirements.

