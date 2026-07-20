# AI21 Labs: List Library Files

Retrieves library files from AI21 Labs.

```
GET https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/list-library-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AI21 Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/list-library-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/list-library-files?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "dataSource": "string",
      "fileId": "string",
      "fileType": "string",
      "labels": [
        "string"
      ],
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "path": "string",
      "publicUrl": "https://example.com",
      "sizeBytes": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string | The creator or owner identifier when available. |
| `creationDate` | date | The file creation timestamp. |
| `dataSource` | string | The file data-source classification when available. |
| `fileId` | string | The AI21 file identifier. |
| `fileType` | string | The file type reported by AI21. |
| `labels` | array<string> | Labels attached to the file. |
| `lastUpdated` | date | The last updated timestamp. |
| `name` | string | The file name. |
| `path` | string | The file path in the AI21 library. |
| `publicUrl` | string | A public URL for the file when available. |
| `sizeBytes` | number | The file size in bytes. |
| `status` | string | The current processing or availability status. |

## Native endpoint

Through the native AI21 Labs API, this operation is `GET /library/files` (base URL `https://api.ai21.com/studio/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-library-files.md) for the provider-specific parameters and requirements.

