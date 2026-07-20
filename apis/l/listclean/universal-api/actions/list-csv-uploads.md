# Listclean: List CSV Uploads

Retrieves saved CSV uploads from Listclean.

```
GET https://connect.mindcloud.co/v1/universal/listclean/latest/actions/list-csv-uploads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listclean `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/list-csv-uploads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/listclean/latest/actions/list-csv-uploads?${params}`, {
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
| `separator_char` | string | CSV separator character. |
| `stage` | string | Current processing stage. |
| `status` | string | Upload status. |
| `total_records` | number | Total records reported by Listclean. |
| `upload_session_id` | string | Provider upload session ID. |

## Native endpoint

Through the native Listclean API, this operation is `GET /uploads/` (base URL `https://api.listclean.xyz/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-csv-uploads.md) for the provider-specific parameters and requirements.

