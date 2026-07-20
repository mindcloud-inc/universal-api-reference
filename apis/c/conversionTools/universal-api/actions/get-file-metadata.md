# Conversion Tools: Get File Metadata

Retrieves file metadata from Conversion Tools.

```
GET https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/get-file-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conversion Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/get-file-metadata?connectionId=$CONNECTION_ID&fileId=b9bc512328764d5da56952ca39f82419" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "b9bc512328764d5da56952ca39f82419"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/get-file-metadata?${params}`, {
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
| `fileId` | string | yes | The file ID to inspect. Example: `b9bc512328764d5da56952ca39f82419`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "previewData": "string",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Provider filename. |
| `previewData` | string | Provider preview text when available. |
| `size` | number | File size in bytes. |

## Native endpoint

Through the native Conversion Tools API, this operation is `GET /files/:fileId/info` (base URL `https://api.conversiontools.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-metadata.md) for the provider-specific parameters and requirements.

