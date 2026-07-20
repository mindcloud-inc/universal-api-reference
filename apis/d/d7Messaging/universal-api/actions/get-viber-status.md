# D7 Messaging: Get Viber Status

Retrieves Viber delivery status from D7 Messaging.

```
GET https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-viber-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-viber-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-viber-status?${params}`, {
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
| `requestId` | string | yes | Request ID returned by Send Viber Message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "messages": [
        {
          "country": "string",
          "msg_id": "string",
          "number_of_viber_message": 1,
          "recipient": "string",
          "schedule_time": "string",
          "status": "string",
          "viber_cost": 1
        }
      ],
      "request_id": "string",
      "total_recipients": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `messages[].country` | string |  |
| `messages[].msg_id` | string |  |
| `messages[].number_of_viber_message` | number |  |
| `messages[].recipient` | string |  |
| `messages[].schedule_time` | string |  |
| `messages[].status` | string |  |
| `messages[].viber_cost` | number |  |
| `request_id` | string |  |
| `total_recipients` | number |  |

## Native endpoint

Through the native D7 Messaging API, this operation is `GET /report/v1/viber-log/:request_id` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-viber-status.md) for the provider-specific parameters and requirements.

