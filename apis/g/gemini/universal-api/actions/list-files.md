# Gemini: List Files

Retrieves a list of files from Gemini.

```
GET https://connect.mindcloud.co/v1/universal/gemini/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gemini/latest/actions/list-files?${params}`, {
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
      "createTime": "2026-05-07T12:00:00.000Z",
      "expirationTime": "2026-05-07T12:00:00.000Z",
      "mimeType": "string",
      "name": "Ava Chen",
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
| `expirationTime` | date | Expiration timestamp. |
| `mimeType` | string | MIME type of the file. |
| `name` | string | File resource name. |
| `sizeBytes` | number | File size in bytes. |
| `source` | string | File source classification. |
| `state` | string | File processing state. |
| `updateTime` | date | Last update timestamp. |
| `uri` | string | File URI. |

## Native endpoint

Through the native Gemini API, this operation is `GET v1beta/files` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

