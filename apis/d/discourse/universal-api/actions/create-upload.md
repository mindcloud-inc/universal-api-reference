# Discourse: Create Upload

Creates a new upload in Discourse.

```
POST https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "type": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "type": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | yes | Binary file payload for the multipart upload. |
| `synchronous` | boolean | no | Whether to return an upload id and URL immediately. |
| `type` | string | yes | Upload type. One of: `0`, `1`, `2`, `3`, `4`. |
| `user_id` | number | no | Required when uploading an avatar. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filesize": 1,
      "human_filesize": "string",
      "id": 1,
      "original_filename": "Ava Chen",
      "short_url": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filesize` | number |  |
| `human_filesize` | string |  |
| `id` | number |  |
| `original_filename` | string |  |
| `short_url` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Discourse API, this operation is `POST /uploads.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-upload.md) for the provider-specific parameters and requirements.

