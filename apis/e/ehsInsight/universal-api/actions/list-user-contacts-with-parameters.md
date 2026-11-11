# EHS Insight: List User Contacts with Parameters



```
GET https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/list-user-contacts-with-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EHS Insight `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/list-user-contacts-with-parameters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/list-user-contacts-with-parameters?${params}`, {
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
| `fields` | string | no | Comma-separated root-level fields to return. Related captions may be requested with dot notation. This does not fetch the full record. Example: `UserContactNumber,FullName,UpdatedDtm`. |
| `updatedBefore` | date | no | Return records modified before this UTC date/time. Example: `2026-01-01T00:00:00Z`. |
| `updatedAfter` | date | no | Return records modified after this UTC date/time. Example: `2026-01-01T00:00:00Z`. |
| `createdBefore` | date | no | Return records created before this UTC date/time. Example: `2026-01-01T00:00:00Z`. |
| `createdAfter` | date | no | Return records created after this UTC date/time. Example: `2026-01-01T00:00:00Z`. |
| `changeTokenBefore` | string | no | Return records with a change token before this token. Example: `20160412.2005544641`. |
| `changeTokenAfter` | string | no | Return newer records ordered by change token ascending. Use the last returned token for the next call. Example: `20160412.2005544641`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authProvider": "string",
      "birthDate": "2026-05-07T12:00:00.000Z",
      "businessEntity": "string",
      "changeToken": "string",
      "createdDtm": "2026-05-07T12:00:00.000Z",
      "emailAddress": "ava@example.com",
      "employeeID": "string",
      "employer": "string",
      "entityName": "Ava Chen",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "gender": "string",
      "hireDate": "2026-05-07T12:00:00.000Z",
      "homeAddress": "string",
      "homeCity": "string",
      "homeState": "string",
      "homeZip": "string",
      "industryStartDate": "2026-05-07T12:00:00.000Z",
      "inviteSent": 1,
      "isEnabled": 1,
      "language": "string",
      "lastName": "Chen",
      "mobilePhoneNumber": "string",
      "phoneNumber": "string",
      "position": "string",
      "positionStartDate": "2026-05-07T12:00:00.000Z",
      "roleAssignmentType": "string",
      "rowUID": "string",
      "supervisor": "string",
      "uIMode": "string",
      "updatedDtm": "2026-05-07T12:00:00.000Z",
      "userContactNumber": "string",
      "userContactPhoto": "string",
      "userContactType": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authProvider` | string |  |
| `birthDate` | date |  |
| `businessEntity` | string |  |
| `changeToken` | string |  |
| `createdDtm` | date |  |
| `emailAddress` | string |  |
| `employeeID` | string |  |
| `employer` | string |  |
| `entityName` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `gender` | string |  |
| `hireDate` | date |  |
| `homeAddress` | string |  |
| `homeCity` | string |  |
| `homeState` | string |  |
| `homeZip` | string |  |
| `industryStartDate` | date |  |
| `inviteSent` | number |  |
| `isEnabled` | number |  |
| `language` | string |  |
| `lastName` | string |  |
| `mobilePhoneNumber` | string |  |
| `phoneNumber` | string |  |
| `position` | string |  |
| `positionStartDate` | date |  |
| `roleAssignmentType` | string |  |
| `rowUID` | string |  |
| `supervisor` | string |  |
| `uIMode` | string |  |
| `updatedDtm` | date |  |
| `userContactNumber` | string |  |
| `userContactPhoto` | string |  |
| `userContactType` | string |  |
| `username` | string |  |

## Native endpoint

Through the native EHS Insight API, this operation is `GET /v6/entity/UserContact/list` (base URL `https://{{credentials.companyName}}.ehsinsight.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-contacts-with-parameters.md) for the provider-specific parameters and requirements.

