# Notifyre SMS: Get Sent SMS Recipient

Retrieves sent SMS recipient details from Notifyre.

```
GET https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-sent-sms-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-sent-sms-recipient?connectionId=$CONNECTION_ID&messageId=string&recipientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string",
  "recipientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-sent-sms-recipient?${params}`, {
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
| `messageId` | string | yes | Sent message identifier. |
| `recipientId` | string | yes | Recipient identifier on the sent message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "friendlyID": "string",
      "id": "string",
      "recipient": {},
      "status": "string",
      "totalCost": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `friendlyID` | string | Human-friendly sent SMS reference. |
| `id` | string | Sent SMS record identifier. |
| `recipient` | object | Recipient delivery details. |
| `status` | string | Delivery status for the recipient. |
| `totalCost` | number | Cost for the recipient delivery. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `GET /sms/send/:messageId/recipients/:recipientId` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sent-sms-recipient.md) for the provider-specific parameters and requirements.

