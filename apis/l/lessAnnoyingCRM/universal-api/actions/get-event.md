# Less Annoying CRM: Get Event



```
GET https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Less Annoying CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/get-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/get-event?${params}`, {
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
| `eventId` | string | yes | The event Id to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": [
        {
          "attendanceStatus": "string",
          "attendeeId": "string",
          "isUser": true
        }
      ],
      "calendarId": "string",
      "calendarMetaData": {
        "name": "Ava Chen"
      },
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "eventId": "string",
      "isAllDay": true,
      "isRecurring": true,
      "location": "string",
      "name": "Ava Chen",
      "recurrenceRule": "string",
      "seriesNumber": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "userIds": [
        "string"
      ],
      "userMetaData": [
        {
          "firstName": "Ava",
          "lastName": "Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees[].attendanceStatus` | string |  |
| `attendees[].attendeeId` | string |  |
| `attendees[].isUser` | boolean |  |
| `calendarId` | string |  |
| `calendarMetaData.name` | string |  |
| `dateCreated` | date |  |
| `dateUpdated` | date |  |
| `description` | string |  |
| `endDate` | date |  |
| `eventId` | string |  |
| `isAllDay` | boolean |  |
| `isRecurring` | boolean |  |
| `location` | string |  |
| `name` | string |  |
| `recurrenceRule` | string |  |
| `seriesNumber` | number |  |
| `startDate` | date |  |
| `userIds[]` | string |  |
| `userMetaData[].firstName` | string |  |
| `userMetaData[].lastName` | string |  |

## Native endpoint

Through the native Less Annoying CRM API, this operation is `POST /` (base URL `https://api.lessannoyingcrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

