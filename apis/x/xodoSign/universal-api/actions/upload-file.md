# Xodo Sign: Upload File

Uploads a file to Xodo Sign.

```
POST https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "business_id": "string",
  "upload": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "business_id": "string",
    "upload": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `business_id` | string | yes | The Xodo Sign business ID that owns the uploaded file. |
| `upload` | file | yes | The file to upload as multipart form-data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file_id": "string",
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file_id` | string | Unique identifier of the uploaded file. |
| `total_pages` | number | Number of pages in the uploaded file. |

## Native endpoint

Through the native Xodo Sign API, this operation is `POST /file` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

