# Tako: Get File

Retrieves file metadata from Tako.

```
GET https://connect.mindcloud.co/v1/universal/tako/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tako `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tako/latest/actions/get-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tako/latest/actions/get-file?${params}`, {
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
| `fileId` | string | yes | ID of the Tako file to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cleaned": true,
      "connected_private_index": "string",
      "file_context": "string",
      "file_id": "string",
      "file_url": "https://example.com",
      "key": "string",
      "last_updated_at": "2026-05-07T12:00:00.000Z",
      "og_key": "string",
      "schema": {},
      "segment_id": "string",
      "source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cleaned` | boolean | Whether the file has been cleaned |
| `connected_private_index` | string | Connected private index identifier |
| `file_context` | string | File context |
| `file_id` | string | Dataset file identifier |
| `file_url` | string | File URL |
| `key` | string | Current file key |
| `last_updated_at` | date | Last updated timestamp |
| `og_key` | string | Original file key |
| `schema` | object | Associated schema metadata |
| `segment_id` | string | Segment identifier |
| `source` | string | Source of the file |

## Native endpoint

Through the native Tako API, this operation is `GET /v1/beta/files/{file_id}/` (base URL `https://tako.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

