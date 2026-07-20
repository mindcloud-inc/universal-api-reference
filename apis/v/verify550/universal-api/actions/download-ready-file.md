# Verify550: Download Ready File

Downloads a ready verification file from Verify550.

```
GET https://connect.mindcloud.co/v1/universal/verify550/latest/actions/download-ready-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verify550 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verify550/latest/actions/download-ready-file?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verify550/latest/actions/download-ready-file?${params}`, {
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
| `id` | string | yes | Verify550 file identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": {
        "clean_file": "string",
        "filename": "Ava Chen",
        "full_file": "string",
        "id": 1,
        "job_id": 1,
        "lines": 1,
        "status": "string",
        "timestamp": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `result.clean_file` | string |  |
| `result.filename` | string |  |
| `result.full_file` | string |  |
| `result.id` | number |  |
| `result.job_id` | number |  |
| `result.lines` | number |  |
| `result.status` | string |  |
| `result.timestamp` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Verify550 API, this operation is `GET /details` (base URL `https://app.verify550.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-ready-file.md) for the provider-specific parameters and requirements.

