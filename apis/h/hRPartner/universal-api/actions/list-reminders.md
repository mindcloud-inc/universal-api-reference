# HR Partner: List Reminders



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-reminders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-reminders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-reminders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native HR Partner API, this operation is `GET /reminders` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reminders.md) for the provider-specific parameters and requirements.

