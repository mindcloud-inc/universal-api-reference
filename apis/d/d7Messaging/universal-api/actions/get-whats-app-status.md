# D7 Messaging: Get WhatsApp Status

Retrieves WhatsApp delivery status from D7 Messaging.

```
GET https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-whats-app-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-whats-app-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-whats-app-status?${params}`, {
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
| `requestId` | string | yes | Request ID returned by the WhatsApp send action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messages": [
        {
          "conversation_type": "string",
          "message_type": "string",
          "msg_id": "string",
          "originator": "string",
          "reason": "string",
          "recipient": "string",
          "reference": {
            "conversation_id": "string",
            "cust_ref": "string",
            "message_tag1": "string",
            "message_tag2": "string",
            "message_tag3": "string",
            "message_tag4": "string",
            "message_tag5": "string"
          },
          "status": "string",
          "template_id": "string",
          "waConvId": "string"
        }
      ],
      "request_id": "string",
      "request_stage": "string",
      "schedule_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messages[].conversation_type` | string |  |
| `messages[].message_type` | string |  |
| `messages[].msg_id` | string |  |
| `messages[].originator` | string |  |
| `messages[].reason` | string |  |
| `messages[].recipient` | string |  |
| `messages[].reference.conversation_id` | string |  |
| `messages[].reference.cust_ref` | string |  |
| `messages[].reference.message_tag1` | string |  |
| `messages[].reference.message_tag2` | string |  |
| `messages[].reference.message_tag3` | string |  |
| `messages[].reference.message_tag4` | string |  |
| `messages[].reference.message_tag5` | string |  |
| `messages[].status` | string |  |
| `messages[].template_id` | string |  |
| `messages[].waConvId` | string |  |
| `request_id` | string |  |
| `request_stage` | string |  |
| `schedule_time` | string |  |

## Native endpoint

Through the native D7 Messaging API, this operation is `GET /whatsapp/v2/report/:request_id` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-whats-app-status.md) for the provider-specific parameters and requirements.

