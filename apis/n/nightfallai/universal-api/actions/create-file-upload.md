# Nightfall.ai: Create File Upload

Creates a file upload in Nightfall.ai.

```
POST https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/create-file-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nightfall.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/create-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileSizeBytes": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/create-file-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileSizeBytes": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileSizeBytes` | number | yes | Total size of the file in bytes. |
| `mimeType` | string | no | Optional MIME type for the file upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chunkSize": 1,
      "fileSizeBytes": 1,
      "id": "string",
      "mimeType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chunkSize` | number | Maximum chunk size in bytes accepted by Nightfall. |
| `fileSizeBytes` | number | Total file size in bytes accepted for the upload. |
| `id` | string | Nightfall file upload UUID. |
| `mimeType` | string | Resolved MIME type for the upload. |

## Native endpoint

Through the native Nightfall.ai API, this operation is `POST /v3/upload` (base URL `https://api.nightfall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file-upload.md) for the provider-specific parameters and requirements.

