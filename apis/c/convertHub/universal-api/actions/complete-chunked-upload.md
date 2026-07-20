# ConvertHub: Complete Chunked Upload

Completes a chunked upload and starts conversion in ConvertHub.

```
PUT https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/complete-chunked-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/complete-chunked-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "upload_987f6543-a21b-98c7-d654-321098765432"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/complete-chunked-upload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "upload_987f6543-a21b-98c7-d654-321098765432"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | Example: `upload_987f6543-a21b-98c7-d654-321098765432`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_id": "string",
      "links": {
        "cancel": "https://example.com",
        "status": "https://example.com"
      },
      "message": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job_id` | string |  |
| `links` | object |  |
| `links.cancel` | string |  |
| `links.status` | string |  |
| `message` | string |  |
| `status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ConvertHub API, this operation is `POST /v2/upload/:sessionId/complete` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-chunked-upload.md) for the provider-specific parameters and requirements.

