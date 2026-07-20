# CoachAccountable: Enroll Client in Course

Enrolls a client in a CoachAccountable course.

```
POST https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/enroll-client-in-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/enroll-client-in-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1,
  "courseId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/enroll-client-in-course', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1,
    "courseId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | yes | The ID of the Client to be added. |
| `courseId` | number | yes | The ID of the Course to which the Client is to be added. |
| `startDate` | date | no | A [future] date at which the Client is to start the Course. If not supplied (or not in the future) the Client will start the Course immediately. |
| `startOnDay` | number | no | Assuming an immediate start, you can supply startOnDay to jump a participant to some other Day in the Course [other than the usual Day 1 start]. |
| `dispatchEarlierStartDayItems` | boolean | no | Assuming an immediate start, you can have or skip items from the start day in the Course be dispatched (e.g. a Message set to go out at 9am if the Client is starting at 11am: should they get that message?). Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CourseParticipantID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CourseParticipantID` | number |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enroll-client-in-course.md) for the provider-specific parameters and requirements.

