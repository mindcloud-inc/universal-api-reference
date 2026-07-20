# Listclean: Start Upload

Starts a CSV upload in Listclean.

```
POST https://connect.mindcloud.co/v1/universal/listclean/latest/actions/start-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listclean `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/start-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "My file.csv",
  "file_type": "csv",
  "total_chunk_count": "24",
  "max_chunk_size": "64000",
  "email_column_index": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/listclean/latest/actions/start-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "My file.csv",
    "file_type": "csv",
    "total_chunk_count": "24",
    "max_chunk_size": "64000",
    "email_column_index": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | CSV file name. Example: `My file.csv`. |
| `file_type` | string | yes | File type, for example csv. Default: `csv`. |
| `total_chunk_count` | number | yes | Total number of chunks for the upload. Example: `24`. |
| `max_chunk_size` | number | yes | Maximum chunk size in bytes. Example: `64000`. |
| `email_column_index` | number | yes | Zero-based index of the CSV column that contains email addresses. Runtime required by Listclean even though the current OpenAPI request schema omits it. Example: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `separator_char` | string | no | CSV separator character. Default: `,`. |
| `enclosure_char` | string | no | Optional field enclosure character, one single-byte character only. |
| `escape_char` | string | no | Optional escape character. An empty value disables escaping. |
| `fast_process` | number | no | Set to 1 for faster processing that avoids slower operations such as SMTP validation; default is 0. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "upload_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `upload_id` | number | Upload ID created for the chunked CSV upload. |

## Native endpoint

Through the native Listclean API, this operation is `POST /uploads/` (base URL `https://api.listclean.xyz/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-upload.md) for the provider-specific parameters and requirements.

