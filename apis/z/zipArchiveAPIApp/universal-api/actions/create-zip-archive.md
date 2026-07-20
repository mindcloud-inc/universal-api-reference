# Zip Archive API app: Create ZIP Archive

Creates a ZIP archive in Zip Archive API app.

```
POST https://connect.mindcloud.co/v1/universal/zipArchiveAPIApp/latest/actions/create-zip-archive
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zip Archive API app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zipArchiveAPIApp/latest/actions/create-zip-archive" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipArchiveAPIApp/latest/actions/create-zip-archive', {
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
| `files[]` | array<string> | no | One or more file URLs to include in the ZIP archive. Example: `https://example.com/file.pdf`. |
| `password` | string | no | Optional password to protect the ZIP archive. Example: `123456`. |
| `compressionLevel` | number | no | Optional ZIP compression level from 1 to 9. Example: `9`. |
| `archiveName` | string | no | Optional output ZIP file name. Example: `result.zip`. |

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
| `response` | object | Raw ZIP archive response payload encoded as a Buffer wrapper. |
| `response.data[]` | array<number> | Raw ZIP response bytes. |
| `response.type` | string | Runtime wrapper type for the binary ZIP response. |

## Native endpoint

Through the native Zip Archive API app API, this operation is `POST /zip` (base URL `https://api.archiveapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-zip-archive.md) for the provider-specific parameters and requirements.

