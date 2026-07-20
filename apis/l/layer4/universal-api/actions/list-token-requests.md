# Layer4: List Token Requests

Retrieves token requests from a Layer4 bucket.

```
GET https://connect.mindcloud.co/v1/universal/layer4/latest/actions/list-token-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Layer4 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/layer4/latest/actions/list-token-requests?connectionId=$CONNECTION_ID&limit=25&offset=0&bucketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "bucketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/layer4/latest/actions/list-token-requests?${params}`, {
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
| `status[]` | array<string> | no | Filter token requests by one or more statuses. |
| `type[]` | array<string> | no | Filter token requests by one or more request types. |

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

Through the native Layer4 API, this operation is `GET /api/v1/buckets/:bucketId/token-requests` (base URL `https://www.layer4.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-token-requests.md) for the provider-specific parameters and requirements.

