# Zoho Connect: Add Event Reminder

Adds a reminder to an event in Zoho Connect.

```
POST https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-event-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-event-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scopeId": "string",
  "streamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-event-reminder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scopeId": "string",
    "streamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scopeId` | string | yes |  |
| `streamId` | string | yes |  |
| `intervalDay` | number | no |  |
| `intervalMinute` | number | no |  |
| `intervalHour` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addEventReminder": {
        "alarm": {
          "alert": [
            {}
          ]
        },
        "result": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addEventReminder.alarm.alert` | array<object> |  |
| `addEventReminder.result` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `POST /pulse/api/addEventReminder` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-event-reminder.md) for the provider-specific parameters and requirements.

