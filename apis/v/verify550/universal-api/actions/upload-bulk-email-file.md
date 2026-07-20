# Verify550: Upload Bulk Email File

Uploads a bulk email file to Verify550.

```
POST https://connect.mindcloud.co/v1/universal/verify550/latest/actions/upload-bulk-email-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verify550 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/verify550/latest/actions/upload-bulk-email-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen",
  "file_contents": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verify550/latest/actions/upload-bulk-email-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen",
    "file_contents": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | Name to assign to the uploaded bulk email file. |
| `file_contents` | file | yes | CSV or text file containing email addresses for bulk verification. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "id": 1,
      "jobId": 1,
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string |  |
| `id` | number |  |
| `jobId` | number |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Verify550 API, this operation is `POST /bulk` (base URL `https://app.verify550.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-bulk-email-file.md) for the provider-specific parameters and requirements.

