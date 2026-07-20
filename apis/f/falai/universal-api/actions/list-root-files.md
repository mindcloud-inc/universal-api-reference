# fal.ai: List Root Files

Retrieves root storage files from fal.ai.

```
GET https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-root-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-root-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-root-files?${params}`, {
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
      "checksum_md5": "string",
      "checksum_sha256": "string",
      "created_time": "2026-05-07T12:00:00.000Z",
      "is_file": true,
      "name": "Ava Chen",
      "path": "string",
      "size": 1,
      "updated_time": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checksum_md5` | string |  |
| `checksum_sha256` | string |  |
| `created_time` | date |  |
| `is_file` | boolean |  |
| `name` | string |  |
| `path` | string |  |
| `size` | number |  |
| `updated_time` | date |  |

## Native endpoint

Through the native fal.ai API, this operation is `GET /serverless/files/list` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-root-files.md) for the provider-specific parameters and requirements.

