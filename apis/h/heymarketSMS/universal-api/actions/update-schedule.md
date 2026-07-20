# Heymarket SMS: Update Schedule



```
PUT https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/update-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/update-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scheduleId": 1,
  "inboxId": 1,
  "executeAt": "string",
  "content.text": "Updated scheduled follow-up"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/update-schedule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scheduleId": 1,
    "inboxId": 1,
    "executeAt": "string",
    "content.text": "Updated scheduled follow-up"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scheduleId` | number | yes | Unique identifier of the schedule. |
| `inboxId` | number | yes | Unique identifier for the inbox from which the scheduled message will be sent. |
| `executeAt` | string | yes | Time at which the message will be sent in RFC 3339 format. |
| `phoneNumber` | string | no | Target phone number in E.164 format without the plus sign. Example: `15555550123`. |
| `content.text` | string | yes | Text content of the scheduled message. Example: `Updated scheduled follow-up`. |
| `content.to` | string | no | Recipient echoed inside the scheduled content object. Example: `15555550123`. |
| `localId` | string | no | Client unique identifier for the scheduled message. Example: `schedule-003`. |
| `userId` | number | no | Sender user ID. Defaults to the team owner if omitted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `PUT /v1/schedule/:id` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-schedule.md) for the provider-specific parameters and requirements.

