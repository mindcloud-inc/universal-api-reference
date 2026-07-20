# fal.ai: List Directory Files

Retrieves storage files from a fal.ai directory.

```
GET https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-directory-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-directory-files?connectionId=$CONNECTION_ID&dir=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dir": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-directory-files?${params}`, {
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
| `dir` | string | yes | Serverless directory path to list. |

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

Through the native fal.ai API, this operation is `GET /serverless/files/list/:dir` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-directory-files.md) for the provider-specific parameters and requirements.

