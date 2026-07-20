# Layer4: Async Create Record

Creates a new record asynchronously in a Layer4 bucket.

```
POST https://connect.mindcloud.co/v1/universal/layer4/latest/actions/async-create-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Layer4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/layer4/latest/actions/async-create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bucketId": "string",
  "data": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/layer4/latest/actions/async-create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bucketId": "string",
    "data": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucketId` | string | yes | Layer4 bucket ID. |
| `contentType` | string | no | Optional content type. |
| `data` | string | yes | Record data to log on-chain. |
| `encrypt` | boolean | no | Whether to encrypt the data. |
| `segmentId` | string | no | Optional segment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucketId": "string",
      "createdAt": "string",
      "files": [
        {}
      ],
      "id": "string",
      "payload": {},
      "recordId": "string",
      "status": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucketId` | string |  |
| `createdAt` | string |  |
| `files` | array<object> |  |
| `id` | string |  |
| `payload` | object |  |
| `recordId` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Layer4 API, this operation is `POST /api/v1/buckets/:bucketId/async/records` (base URL `https://www.layer4.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/async-create-record.md) for the provider-specific parameters and requirements.

