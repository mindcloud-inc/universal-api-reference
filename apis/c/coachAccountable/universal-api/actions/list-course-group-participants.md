# CoachAccountable: List Course Group Participants

Retrieves course group participants from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-course-group-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-course-group-participants?connectionId=$CONNECTION_ID&courseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-course-group-participants?${params}`, {
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
| `courseId` | number | yes | The ID of the Course whose Participants are to be gotten. |
| `groupId` | number | no | Optionally filter by ID of the Group for whom Participations are to be gotten. |
| `includeCompleted` | boolean | no | Include Participants whose Course timeline progression has already been completed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCompleted": "2026-05-07T12:00:00.000Z",
      "dayOf": 1,
      "groupName": "Ava Chen",
      "ID": 1,
      "includedMembers": [
        {
          "ClientID": 1,
          "clientName": "Ava Chen"
        }
      ],
      "isComplete": true,
      "isPaused": true,
      "startDate": "2026-05-07T12:00:00.000Z",
      "unpauseDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCompleted` | date |  |
| `dayOf` | number |  |
| `groupName` | string |  |
| `ID` | number |  |
| `includedMembers` | array<object> |  |
| `includedMembers[].ClientID` | number |  |
| `includedMembers[].clientName` | string |  |
| `isComplete` | boolean |  |
| `isPaused` | boolean |  |
| `startDate` | date |  |
| `unpauseDate` | date |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-course-group-participants.md) for the provider-specific parameters and requirements.

