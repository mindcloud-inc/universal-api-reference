# CoachAccountable: List Group Client Members

Retrieves group client members from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-group-client-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-group-client-members?connectionId=$CONNECTION_ID&groupId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-group-client-members?${params}`, {
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
| `groupId` | number | yes | The ID of the Group whose Client Members are to be gotten. |
| `includeInactive` | boolean | no | Include Group Clients who are inactive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientFirstName": "Ava",
      "ClientID": 1,
      "clientLastName": "Chen",
      "ID": 1,
      "isActive": true,
      "startDate": "string"
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
| `ID` | number |  |
| `isActive` | boolean |  |
| `startDate` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-client-members.md) for the provider-specific parameters and requirements.

