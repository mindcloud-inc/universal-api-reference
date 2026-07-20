# Customers.ai: Send JSON Message

Sends a JSON message to a contact in Customers.ai.

```
PUT https://connect.mindcloud.co/v1/universal/customersai/latest/actions/send-json-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customers.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/customersai/latest/actions/send-json-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipientId": "string",
  "jsonMessage": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customersai/latest/actions/send-json-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipientId": "string",
    "jsonMessage": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipientId` | string | yes | Recipient ID or contact ID of the contact to message. |
| `jsonMessage` | object | yes | JSON message payload to send to the contact. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Customers.ai API returns.

## Native endpoint

Through the native Customers.ai API, this operation is `POST /contacts/:recipient_id/send_json_message` (base URL `https://api.mobilemonkey.com/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-json-message.md) for the provider-specific parameters and requirements.

