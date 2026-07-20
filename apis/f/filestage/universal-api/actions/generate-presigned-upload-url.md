# Filestage: Generate Presigned Upload URL

Creates a presigned upload URL in Filestage.

```
POST https://connect.mindcloud.co/v1/universal/filestage/latest/actions/generate-presigned-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/generate-presigned-upload-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestage/latest/actions/generate-presigned-upload-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stepId` | string | no | The ID of the step to upload the file to. This field is required when the `projectId` field is empty |
| `projectId` | string | no | The ID of the project to upload the file to. This field is required when the `stepId` field is empty |
| `pregenerateFileId` | boolean | no | When this flag is set to true it generates the ID of the file before it's being uploaded. The `fileId` which is being pre-generated is used as `pregeneratedFileId field in the `POST /files` endpoint.. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileURL": "https://example.com",
      "pregeneratedFileId": "string",
      "uploadURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileURL` | string |  |
| `pregeneratedFileId` | string |  |
| `uploadURL` | string |  |

## Native endpoint

Through the native Filestage API, this operation is `POST /files/upload-url` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-presigned-upload-url.md) for the provider-specific parameters and requirements.

