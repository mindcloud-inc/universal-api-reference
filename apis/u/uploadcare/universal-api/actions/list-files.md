# Uploadcare: List Files

Retrieves all files from your Uploadcare project.

```
GET https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/list-files?${params}`, {
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
| `from` | date | no | Start listing files uploaded after this ISO 8601 timestamp. |
| `include` | string | no | Include extra fields such as appdata in the file object. |
| `ordering` | string | no | Sort order for returned files. |
| `removed` | boolean | no | Set true to only include removed files. |
| `stored` | boolean | no | Set true to only include stored files, or false for temporary files. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentInfo": {},
      "datetimeRemoved": "2026-05-07T12:00:00.000Z",
      "datetimeStored": "2026-05-07T12:00:00.000Z",
      "datetimeUploaded": "2026-05-07T12:00:00.000Z",
      "isImage": true,
      "isReady": true,
      "metadata": {},
      "mimeType": "string",
      "originalFilename": "Ava Chen",
      "originalFileUrl": "https://example.com",
      "size": 1,
      "url": "https://example.com",
      "uuid": "string",
      "variations": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentInfo` | object |  |
| `datetimeRemoved` | date |  |
| `datetimeStored` | date |  |
| `datetimeUploaded` | date |  |
| `isImage` | boolean |  |
| `isReady` | boolean |  |
| `metadata` | object |  |
| `mimeType` | string |  |
| `originalFilename` | string |  |
| `originalFileUrl` | string |  |
| `size` | number |  |
| `url` | string |  |
| `uuid` | string |  |
| `variations` | object |  |

## Native endpoint

Through the native Uploadcare API, this operation is `GET /files/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

