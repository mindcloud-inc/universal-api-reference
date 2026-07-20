# Layer4: Get Token Request

Retrieves a token request from a Layer4 bucket.

```
GET https://connect.mindcloud.co/v1/universal/layer4/latest/actions/get-token-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Layer4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/layer4/latest/actions/get-token-request?connectionId=$CONNECTION_ID&bucketId=string&tokenRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucketId": "string",
  "tokenRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/layer4/latest/actions/get-token-request?${params}`, {
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
| `bucketId` | string | yes | The Layer4 bucket identifier. |
| `tokenRequestId` | string | yes | The Layer4 token request identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucketId": "string",
      "files": [
        {}
      ],
      "id": "string",
      "image": {},
      "payload": {},
      "status": "string",
      "tokenId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucketId` | string |  |
| `files` | array<object> |  |
| `id` | string |  |
| `image` | object |  |
| `payload` | object |  |
| `status` | string |  |
| `tokenId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Layer4 API, this operation is `GET /api/v1/buckets/:bucketId/token-requests/:tokenRequestId` (base URL `https://www.layer4.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-request.md) for the provider-specific parameters and requirements.

