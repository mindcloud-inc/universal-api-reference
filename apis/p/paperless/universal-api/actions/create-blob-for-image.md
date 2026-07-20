# Paperless: Create Blob For Image



```
POST https://connect.mindcloud.co/v1/universal/paperless/latest/actions/create-blob-for-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paperless/latest/actions/create-blob-for-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "byteSize": 1,
  "checksum": "string",
  "contentType": "string",
  "filename": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paperless/latest/actions/create-blob-for-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "byteSize": 1,
    "checksum": "string",
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
| `byteSize` | number | yes | The size of the blob in bytes. |
| `checksum` | string | yes | The content checksum expected by Paperless. |
| `contentType` | string | yes | The blob MIME type. |
| `filename` | string | yes | The filename to register for the blob. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachable_sgid": "string",
      "byte_size": 1,
      "checksum": "string",
      "content_type": "string",
      "created_at": "string",
      "direct_upload": {},
      "filename": "Ava Chen",
      "id": 1,
      "key": "string",
      "metadata": {},
      "service_name": "Ava Chen",
      "signed_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachable_sgid` | string |  |
| `byte_size` | number |  |
| `checksum` | string |  |
| `content_type` | string |  |
| `created_at` | string |  |
| `direct_upload` | object |  |
| `filename` | string |  |
| `id` | number |  |
| `key` | string |  |
| `metadata` | object |  |
| `service_name` | string |  |
| `signed_id` | string |  |

## Native endpoint

Through the native Paperless API, this operation is `POST /blobs` (base URL `https://app.paperless.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-blob-for-image.md) for the provider-specific parameters and requirements.

