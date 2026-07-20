# CoachAccountable: List Group Coach Members

Retrieves group coach members from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-group-coach-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-group-coach-members?connectionId=$CONNECTION_ID&groupId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-group-coach-members?${params}`, {
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
| `groupId` | number | yes | The ID of the Group whose Coach Members are to be gotten. |
| `includeInactive` | boolean | no | Include Group Coaches who are inactive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "coachFirstName": "Ava",
      "CoachID": 1,
      "coachLastName": "Chen",
      "ID": 1,
      "isActive": true,
      "isOwner": true,
      "startDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coachFirstName` | string |  |
| `CoachID` | number |  |
| `coachLastName` | string |  |
| `ID` | number |  |
| `isActive` | boolean |  |
| `isOwner` | boolean |  |
| `startDate` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-coach-members.md) for the provider-specific parameters and requirements.

