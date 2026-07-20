# Open AI: List Files

Retrieves files from Open AI.

```
GET https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-files?${params}`, {
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
| `limit` | number | no | Maximum number of files to return. Default: `20`. |
| `order` | string | no | Sort order by created time. Default: `desc`. |
| `purpose` | string | no | Only return files with the given purpose. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "bytes": 1,
          "filename": "Ava Chen",
          "id": "string",
          "object": "string",
          "purpose": "string",
          "status": "string"
        }
      ],
      "first_id": "string",
      "has_more": true,
      "last_id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Returned files. |
| `data[].bytes` | number | File size in bytes. |
| `data[].filename` | string | Filename. |
| `data[].id` | string | File ID. |
| `data[].object` | string | Object type. |
| `data[].purpose` | string | File purpose. |
| `data[].status` | string | File processing status. |
| `first_id` | string | First returned file ID. |
| `has_more` | boolean | Whether more files are available. |
| `last_id` | string | Last returned file ID. |
| `object` | string | List object type. |

## Native endpoint

Through the native Open AI API, this operation is `GET v1/files` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

