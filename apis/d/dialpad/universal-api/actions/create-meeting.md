# Dialpad: Create Meeting

Creates a new meeting in Dialpad.

```
POST https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "6236728822472704",
  "title": "MindCloud test meeting",
  "meetingType": "CUSTOM_UNIQUE_MEETING",
  "startDatetime": "2026-03-20T15:00:00Z",
  "endDatetime": "2026-03-20T15:30:00Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-meeting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "6236728822472704",
    "title": "MindCloud test meeting",
    "meetingType": "CUSTOM_UNIQUE_MEETING",
    "startDatetime": "2026-03-20T15:00:00Z",
    "endDatetime": "2026-03-20T15:30:00Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes | The Dialpad user's id. Example: `6236728822472704`. |
| `title` | string | yes | The meeting's title. Example: `MindCloud test meeting`. |
| `meetingType` | list<string> | yes | The meeting's type. One of: `CUSTOM_UNIQUE_MEETING`, `LARGE_MEETING`, `PERSONAL`, `UNIQUE_MEETING`. |
| `startDatetime` | date | yes | The meeting's start time (UTC seconds-since-epoch timestamp). Example: `2026-03-20T15:00:00Z`. |
| `endDatetime` | date | yes | The meeting's end time (UTC seconds-since-epoch timestamp). Example: `2026-03-20T15:30:00Z`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `duration` | number | no | Duration of the meeting in seconds. Example: `1800`. |
| `callOut` | boolean | no | Whether or not the meeting should call the participants. |
| `recurrence` | string | no | How often the meeting should be repeated. Example: `FREQ=WEEKLY;COUNT=4`. |
| `participantsInfo[]` | array<object> | no | The list of users that participate in the meeting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callOut": true,
      "dialInNumber": "string",
      "duration": 1,
      "endDatetime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "instanceId": "string",
      "isModerated": true,
      "meetingType": "string",
      "meetingUrl": "https://example.com",
      "organizerPin": "string",
      "participantPin": "string",
      "participantsInfo": [
        {
          "callInMethod": "string",
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "isOrganizer": true,
          "name": "Ava Chen",
          "phone": "string",
          "phoneNumber": "string",
          "talkTime": 1
        }
      ],
      "recurrence": "string",
      "recurrenceEndDate": "2026-05-07T12:00:00.000Z",
      "startDatetime": "2026-05-07T12:00:00.000Z",
      "timezone": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callOut` | boolean |  |
| `dialInNumber` | string |  |
| `duration` | number |  |
| `endDatetime` | date |  |
| `id` | string |  |
| `instanceId` | string |  |
| `isModerated` | boolean |  |
| `meetingType` | string |  |
| `meetingUrl` | string |  |
| `organizerPin` | string |  |
| `participantPin` | string |  |
| `participantsInfo[].callInMethod` | string |  |
| `participantsInfo[].displayName` | string |  |
| `participantsInfo[].email` | string |  |
| `participantsInfo[].isOrganizer` | boolean |  |
| `participantsInfo[].name` | string |  |
| `participantsInfo[].phone` | string |  |
| `participantsInfo[].phoneNumber` | string |  |
| `participantsInfo[].talkTime` | number |  |
| `recurrence` | string |  |
| `recurrenceEndDate` | date |  |
| `startDatetime` | date |  |
| `timezone` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Dialpad API, this operation is `POST /meetings` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-meeting.md) for the provider-specific parameters and requirements.

