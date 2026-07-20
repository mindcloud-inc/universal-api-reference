# Google AI Studio: Get File

Retrieves file metadata from Google AI Studio.

```
GET https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google AI Studio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/get-file?connectionId=$CONNECTION_ID&fileId=files%2Fabc-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "files/abc-123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/get-file?${params}`, {
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
| `fileId` | string | yes | Full file resource name, for example `files/abc-123`. Example: `files/abc-123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "expirationTime": "2026-05-07T12:00:00.000Z",
      "mimeType": "string",
      "name": "Ava Chen",
      "sha256Hash": "string",
      "sizeBytes": 1,
      "source": "string",
      "state": "string",
      "updateTime": "2026-05-07T12:00:00.000Z",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | date | Creation timestamp. |
| `displayName` | string | User-provided file display name. |
| `expirationTime` | date | Expiration timestamp. |
| `mimeType` | string | MIME type of the file. |
| `name` | string | File resource name. |
| `sha256Hash` | string | SHA-256 hash (base64). |
| `sizeBytes` | number | File size in bytes. |
| `source` | string | File source classification. |
| `state` | string | File processing state. |
| `updateTime` | date | Last update timestamp. |
| `uri` | string | File URI. |

## Native endpoint

Through the native Google AI Studio API, this operation is `GET v1beta/files/:fileId` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

