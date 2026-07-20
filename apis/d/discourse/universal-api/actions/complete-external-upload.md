# Discourse: Complete External Upload

Completes an external upload in Discourse.

```
POST https://connect.mindcloud.co/v1/universal/discourse/latest/actions/complete-external-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/complete-external-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "unique_identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/complete-external-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "unique_identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `for_private_message` | string | no | Whether the upload is for a private message. One of: `0`, `1`. |
| `for_site_setting` | string | no | Whether the upload is for a site setting. One of: `0`, `1`. |
| `pasted` | string | no | Whether the upload was pasted into the composer. One of: `0`, `1`. |
| `unique_identifier` | string | yes | The unique identifier returned by Generate Presigned Put. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filesize": 1,
      "height": 1,
      "human_filesize": "string",
      "id": 1,
      "original_filename": "Ava Chen",
      "short_path": "string",
      "short_url": "https://example.com",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filesize` | number |  |
| `height` | number |  |
| `human_filesize` | string |  |
| `id` | number |  |
| `original_filename` | string |  |
| `short_path` | string |  |
| `short_url` | string |  |
| `url` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Discourse API, this operation is `POST /uploads/complete-external-upload.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-external-upload.md) for the provider-specific parameters and requirements.

