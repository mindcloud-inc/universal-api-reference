# CoachAccountable: List Course Client Availabilities

Retrieves course client availabilities from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-course-client-availabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-course-client-availabilities?connectionId=$CONNECTION_ID&clientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-course-client-availabilities?${params}`, {
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
| `clientId` | number | yes | ID of the Client for whom Course Availabilities are to be gotten. |
| `includeUsed` | boolean | no | Include Course Availabilities which have already been used. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientFirstName": "Ava",
      "ClientID": 1,
      "clientLastName": "Chen",
      "CourseID": 1,
      "courseName": "Ava Chen",
      "dateAdded": "2026-05-07T12:00:00.000Z",
      "dateAvailable": "2026-05-07T12:00:00.000Z",
      "dateUsed": "2026-05-07T12:00:00.000Z",
      "ID": 1,
      "isUsed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientFirstName` | string |  |
| `ClientID` | number |  |
| `clientLastName` | string |  |
| `CourseID` | number |  |
| `courseName` | string |  |
| `dateAdded` | date |  |
| `dateAvailable` | date |  |
| `dateUsed` | date |  |
| `ID` | number |  |
| `isUsed` | boolean |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-course-client-availabilities.md) for the provider-specific parameters and requirements.

