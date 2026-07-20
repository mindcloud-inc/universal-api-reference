# ForceManager: Update Calendar

Updates an existing calendar in ForceManager.

```
PUT https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-calendar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-calendar', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Unique identifier for the calendar. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "accountName": "Ava Chen",
      "activityTypeId": 1,
      "activityTypeName": "Ava Chen",
      "allDay": true,
      "contactId": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "deleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | ID of the account associated to this calendar. |
| `accountName` | string | Name of the account associated to this calendar. |
| `activityTypeId` | number | ID of the activity type related to the calendar. |
| `activityTypeName` | string | Description of the activity type related to the calendar. |
| `allDay` | boolean | Whether the calendar is for the whole day. |
| `contactId` | number | ID of the contact associated to the calendar. |
| `createdDate` | date | Date of creation of the calendar. |
| `deleted` | boolean | Whether the calendar has been deleted. |

## Native endpoint

Through the native ForceManager API, this operation is `PUT /calendars`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-calendar.md) for the provider-specific parameters and requirements.

