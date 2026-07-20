# D7 Networks: Get WhatsApp Message Status

Retrieves WhatsApp message status from D7 Networks.

```
GET https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-whats-app-message-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-whats-app-message-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-whats-app-message-status?${params}`, {
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
| `requestId` | string | yes | Request ID returned by a WhatsApp send action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recipients": [
        {}
      ],
      "request_id": "string",
      "request_stage": "string",
      "schedule_time": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recipients` | array<object> |  |
| `request_id` | string |  |
| `request_stage` | string |  |
| `schedule_time` | date |  |

## Native endpoint

Through the native D7 Networks API, this operation is `GET /whatsapp/v2/report/:requestId` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-whats-app-message-status.md) for the provider-specific parameters and requirements.

