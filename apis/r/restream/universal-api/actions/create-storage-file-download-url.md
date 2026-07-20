# Restream: Create Storage File Download URL

Generates a download URL for a storage file in Restream.

```
GET https://connect.mindcloud.co/v1/universal/restream/latest/actions/create-storage-file-download-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restream/latest/actions/create-storage-file-download-url?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restream/latest/actions/create-storage-file-download-url?${params}`, {
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
| `fileId` | string | yes | The ID of the storage file whose download URL to generate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "downloadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `downloadUrl` | string |  |

## Native endpoint

Through the native Restream API, this operation is `POST /user/storage/files/:fileId/download-url` (base URL `https://api.restream.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-storage-file-download-url.md) for the provider-specific parameters and requirements.

