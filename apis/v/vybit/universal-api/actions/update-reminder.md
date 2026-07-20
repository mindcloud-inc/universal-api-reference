# Vybit: Update Reminder



```
PUT https://connect.mindcloud.co/v1/universal/vybit/latest/actions/update-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/update-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string",
  "reminderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vybit/latest/actions/update-reminder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string",
    "reminderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cron` | string | no | Updated cron expression |
| `imageUrl` | string | no | Updated image URL |
| `key` | string | yes | The unique key of the vybit. |
| `linkUrl` | string | no | Updated link URL |
| `log` | string | no | Updated log content |
| `message` | string | no | Updated notification message |
| `reminderId` | string | yes | The unique ID of the reminder. |
| `timeZone` | string | no | Updated IANA time zone |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reminder": {},
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reminder` | object |  |
| `result` | number |  |

## Native endpoint

Through the native Vybit API, this operation is `PATCH /vybit/{{key}}/reminders/{{reminderId}}` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reminder.md) for the provider-specific parameters and requirements.

