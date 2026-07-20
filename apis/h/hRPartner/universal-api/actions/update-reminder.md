# HR Partner: Update Reminder



```
PUT https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/update-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/update-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reminderID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/update-reminder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reminderID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reminderID` | string | yes | Reminder ID from HR Partner. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "description": "string",
      "employee": {},
      "id": 1,
      "module": "string",
      "moduleId": 1,
      "notificationSent": true,
      "remindAt": "2026-05-07T12:00:00.000Z",
      "sendNotification": true,
      "setBy": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `description` | string |  |
| `employee` | object |  |
| `id` | number |  |
| `module` | string |  |
| `moduleId` | number |  |
| `notificationSent` | boolean |  |
| `remindAt` | date |  |
| `sendNotification` | boolean |  |
| `setBy` | object |  |

## Native endpoint

Through the native HR Partner API, this operation is `POST /reminder/:reminderID` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reminder.md) for the provider-specific parameters and requirements.

