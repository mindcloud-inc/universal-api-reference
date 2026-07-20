# Zip Archive API app: Extract ZIP Archive

Extracts a ZIP archive in Zip Archive API app.

```
GET https://connect.mindcloud.co/v1/universal/zipArchiveAPIApp/latest/actions/extract-zip-archive
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zip Archive API app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zipArchiveAPIApp/latest/actions/extract-zip-archive?connectionId=$CONNECTION_ID&file=https%3A%2F%2Fgithub.com%2Fgithubtraining%2Fhellogitworld%2Farchive%2Frefs%2Fheads%2Fmaster.zip" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "https://github.com/githubtraining/hellogitworld/archive/refs/heads/master.zip"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zipArchiveAPIApp/latest/actions/extract-zip-archive?${params}`, {
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
| `file` | string | yes | Public URL of the ZIP file to extract. Example: `https://github.com/githubtraining/hellogitworld/archive/refs/heads/master.zip`. |
| `password` | string | no | Optional password for encrypted ZIP files. Example: `123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "data": [
          [
            1
          ]
        ],
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | object | Raw extracted archive response payload encoded as a Buffer wrapper. |
| `response.data[]` | array<number> | Raw extraction response bytes. |
| `response.type` | string | Runtime wrapper type for the binary extraction response. |

## Native endpoint

Through the native Zip Archive API app API, this operation is `POST /extract` (base URL `https://api.archiveapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-zip-archive.md) for the provider-specific parameters and requirements.

