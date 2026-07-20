# Dialpad: Get Meeting

Retrieves detailed meeting information from Dialpad.

```
GET https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-meeting?connectionId=$CONNECTION_ID&id=1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-meeting?${params}`, {
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
| `id` | string | yes | The meeting room's ID. Example: `1234567890`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | no | The Dialpad user's id. Example: `6236728822472704`. |

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

Through the native Dialpad API, this operation is `GET /meetings/:id` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting.md) for the provider-specific parameters and requirements.

