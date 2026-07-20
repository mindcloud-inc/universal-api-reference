# Chatvolt AI: Upload Media

Uploads media to Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-media-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-media-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "artifact_id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-media-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "artifact_id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | yes | File for multipart/form-data requests. |
| `artifact_id` | string | yes | Artifact Id for multipart/form-data requests. |
| `name` | string | yes | Name for multipart/form-data requests. |
| `alt_description` | string | no | Alt Description for multipart/form-data requests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "artifactMedia": {},
      "fileUrl": "https://example.com",
      "s3Key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `artifactMedia` | object | ArtifactMedia. |
| `fileUrl` | string | FileUrl. |
| `s3Key` | string | S3Key. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /artifacts/media/upload` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/artifacts-media-upload.md) for the provider-specific parameters and requirements.

