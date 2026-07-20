# Openlayer: Get Project Version Upload URL

Retrieves a version upload URL for a project in Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-project-version-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-project-version-upload-url?connectionId=$CONNECTION_ID&objectName=mindcloud-extra.bin&projectId=2fcd0a42-23a7-44bb-b4fa-4fc3168fe248&storageInterface=s3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectName": "mindcloud-extra.bin",
  "projectId": "2fcd0a42-23a7-44bb-b4fa-4fc3168fe248",
  "storageInterface": "s3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-project-version-upload-url?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectName` | string | yes | Artifact object name. Default: `mindcloud-extra.bin`. |
| `projectId` | string | yes | The Openlayer project ID. Default: `2fcd0a42-23a7-44bb-b4fa-4fc3168fe248`. |
| `storageInterface` | string | yes | Storage platform for the upload URL. Default: `s3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "storageUri": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `storageUri` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /projects/:projectId/versions/presigned-url` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-version-upload-url.md) for the provider-specific parameters and requirements.

