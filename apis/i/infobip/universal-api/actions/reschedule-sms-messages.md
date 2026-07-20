# Infobip: Reschedule SMS Messages



```
PUT https://connect.mindcloud.co/v1/universal/infobip/latest/actions/reschedule-sms-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/reschedule-sms-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bulkId": "string",
  "sendAt": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/reschedule-sms-messages', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bulkId": "string",
    "sendAt": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bulkId` | string | yes | Unique ID assigned to the request if messaging multiple recipients or sending multiple messages via a single API request. |
| `sendAt` | date | yes | Date and time when the message is to be sent. Used for scheduled SMS (see [Scheduled SMS endpoints](#channels/sms/get-scheduled-sms-messages) for more details). Has the following format: `yyyy-MM-dd'T'HH:mm:ss.SSSZ`, and can only be scheduled for no later than 180 days in advance. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bulkId": "string",
      "sendAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulkId` | string |  |
| `sendAt` | date |  |

## Native endpoint

Through the native Infobip API, this operation is `PUT /sms/1/bulks` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reschedule-sms-messages.md) for the provider-specific parameters and requirements.

