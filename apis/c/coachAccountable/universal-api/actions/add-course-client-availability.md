# CoachAccountable: Add Course Client Availability

Adds course client availability in CoachAccountable.

```
POST https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/add-course-client-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/add-course-client-availability" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1,
  "courseId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/add-course-client-availability', {
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
| `clientId` | number | yes | The ID of the Client to make the Course availabile to. |
| `courseId` | number | yes | The ID of the Course that the Client is to have made available. |
| `dateAvailable` | date | no | A [future] date at which the Client is be able to start the Course. If not supplied (or not in the future) the Course will be made available to the Client immediately. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CourseAvailabilityID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CourseAvailabilityID` | number |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-course-client-availability.md) for the provider-specific parameters and requirements.

