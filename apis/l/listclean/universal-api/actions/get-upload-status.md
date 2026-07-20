# Listclean: Get Upload Status

Retrieves CSV upload status from Listclean.

```
GET https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-upload-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listclean `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-upload-status?connectionId=$CONNECTION_ID&upload_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "upload_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-upload-status?${params}`, {
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
| `upload_id` | number | yes | Upload ID to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chunk_details": {},
      "client_filename": "Ava Chen",
      "count": 1,
      "email_column_index": 1,
      "enclosure_char": "string",
      "entered": "string",
      "escape_char": "string",
      "fast_process": 1,
      "filename": "Ava Chen",
      "id": 1,
      "import_result": {},
      "remarks": "string",
      "request_id": 1,
      "separator_char": "string",
      "stage": "string",
      "status": "string",
      "total_records": 1,
      "upload_session_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chunk_details` | object | Chunk upload count details. |
| `client_filename` | string | Original filename. |
| `count` | number | Processed count. |
| `email_column_index` | number | Zero-based email column index. |
| `enclosure_char` | string | CSV enclosure character. |
| `entered` | string | Upload creation timestamp. |
| `escape_char` | string | CSV escape character. |
| `fast_process` | number | Fast-processing flag. |
| `filename` | string | Stored filename. |
| `id` | number | Upload ID. |
| `import_result` | object | Import result details when available. |
| `remarks` | string | Provider remarks. |
| `request_id` | number | Verification list request ID created from the upload. |
| `separator_char` | string | CSV separator character. |
| `stage` | string | Current processing stage. |
| `status` | string | Upload status. |
| `total_records` | number | Total records reported by Listclean. |
| `upload_session_id` | string | Provider upload session ID. |

## Native endpoint

Through the native Listclean API, this operation is `GET /uploads/:upload_id` (base URL `https://api.listclean.xyz/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upload-status.md) for the provider-specific parameters and requirements.

