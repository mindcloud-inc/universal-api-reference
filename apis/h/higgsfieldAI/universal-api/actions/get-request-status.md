# Higgsfield AI: Get Request Status

Retrieves a generation request status from Higgsfield AI.

```
GET https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/get-request-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Higgsfield AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/get-request-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/get-request-status?${params}`, {
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
| `requestId` | string | yes | Higgsfield request UUID returned by a generation request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancel_url": "https://example.com",
      "error": "string",
      "images": [
        {}
      ],
      "request_id": "string",
      "status": "string",
      "status_url": "https://example.com",
      "video": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancel_url` | string |  |
| `error` | string |  |
| `images` | array<object> |  |
| `request_id` | string |  |
| `status` | string |  |
| `status_url` | string |  |
| `video` | object |  |

## Native endpoint

Through the native Higgsfield AI API, this operation is `GET /requests/{requestId}/status` (base URL `https://platform.higgsfield.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-request-status.md) for the provider-specific parameters and requirements.

