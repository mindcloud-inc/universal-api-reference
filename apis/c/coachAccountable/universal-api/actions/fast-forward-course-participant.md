# CoachAccountable: Fast Forward Course Participant

Fast-forwards a course participant in CoachAccountable.

```
PUT https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/fast-forward-course-participant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/fast-forward-course-participant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseParticipantId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/fast-forward-course-participant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseParticipantId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseParticipantId` | number | yes | The ID of the Participant to be fast forwarded. |
| `days` | number | no | How many days to fast forward? Must be 1 or greater. |
| `dispatchItems` | boolean | no | Should Course items during the fast-forward period be dispatched to this participant? Default: `false`. |
| `issueNotifications` | boolean | no | IF Course items during the fast-forward period should be dispatched, should notifications of them be sent to this participant? Ignored when dispatchItems is false. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CoachAccountable API returns.

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fast-forward-course-participant.md) for the provider-specific parameters and requirements.

