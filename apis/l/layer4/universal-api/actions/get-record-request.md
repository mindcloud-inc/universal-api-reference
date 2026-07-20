# Layer4: Get Record Request

Retrieves a record request from a Layer4 bucket.

```
GET https://connect.mindcloud.co/v1/universal/layer4/latest/actions/get-record-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Layer4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/layer4/latest/actions/get-record-request?connectionId=$CONNECTION_ID&bucketId=string&recordRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucketId": "string",
  "recordRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/layer4/latest/actions/get-record-request?${params}`, {
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
| `bucketId` | string | yes | Layer4 bucket ID. |
| `decrypt` | boolean | no | Whether to decrypt the record request. |
| `recordRequestId` | string | yes | Layer4 record request ID. |

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

Through the native Layer4 API, this operation is `GET /api/v1/buckets/:bucketId/record-requests/:recordRequestId` (base URL `https://www.layer4.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record-request.md) for the provider-specific parameters and requirements.

