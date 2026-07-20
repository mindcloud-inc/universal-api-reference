# Wati: List Messages by WhatsApp Number

Retrieves message history for a WhatsApp number from Wati.

```
GET https://connect.mindcloud.co/v1/universal/wati/latest/actions/list-messages-by-whatsapp-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wati `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wati/latest/actions/list-messages-by-whatsapp-number?connectionId=$CONNECTION_ID&whatsappNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "whatsappNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wati/latest/actions/list-messages-by-whatsapp-number?${params}`, {
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
| `whatsappNumber` | string | yes | WhatsApp phone number whose messages should be retrieved. |
| `pageSize` | number | no | Number of messages to return per page. Default: `10`. |
| `pageNumber` | number | no | Page number to return. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedId": "string",
      "conversationId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "eventDescription": "string",
      "eventType": "string",
      "failedDetail": "string",
      "finalText": "string",
      "id": "string",
      "operatorName": "Ava Chen",
      "owner": true,
      "statusString": "string",
      "text": "string",
      "ticketId": "string",
      "timestamp": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedId` | string | Assigned operator identifier when present. |
| `conversationId` | string | Conversation identifier. |
| `created` | date | When the message or event was created. |
| `eventDescription` | string | Event description when the row is a broadcast or non-message event. |
| `eventType` | string | Normalized event type returned by Wati. |
| `failedDetail` | string | Failure detail when the provider returns one. |
| `finalText` | string | Rendered final text for broadcast/template events. |
| `id` | string | Wati message or event identifier. |
| `operatorName` | string | Assigned operator name when present. |
| `owner` | boolean | Whether the message was sent by the connected account. |
| `statusString` | string | Delivery or event status. |
| `text` | string | Message text when the row is a standard message. |
| `ticketId` | string | Conversation ticket identifier. |
| `timestamp` | string | Provider message timestamp when present. |
| `type` | string | Underlying Wati message type when present. |

## Native endpoint

Through the native Wati API, this operation is `GET /api/v1/getMessages/:whatsappNumber` (base URL `{{credentials.apiEndpointUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages-by-whatsapp-number.md) for the provider-specific parameters and requirements.

