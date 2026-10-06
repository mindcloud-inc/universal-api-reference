# EHS Insight: List User Contacts



```
GET https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/list-user-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EHS Insight `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/list-user-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/list-user-contacts?${params}`, {
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
| `customparams` | string | no | Optional provider-specific query string segment appended after the list route. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rowUID": "string",
      "createdDtm": "string",
      "updatedDtm": "string",
      "changeToken": "string",
      "userContactNumber": "string",
      "userContactType": "string",
      "inviteSent": 1,
      "fullName": "Ava Chen",
      "userContactPhoto": "string",
      "language": "string",
      "uIMode": "string",
      "isEnabled": 1,
      "firstName": "Ava",
      "lastName": "Chen",
      "gender": "string",
      "birthDate": "string",
      "homeAddress": "string",
      "homeCity": "string",
      "homeState": "string",
      "homeZip": "string",
      "phoneNumber": "string",
      "businessEntity": "string",
      "position": "string",
      "employer": "string",
      "supervisor": "string",
      "employeeID": "string",
      "hireDate": "string",
      "positionStartDate": "string",
      "industryStartDate": "string",
      "authProvider": "string",
      "username": "Ava Chen",
      "emailAddress": "ava@example.com",
      "mobilePhoneNumber": "string",
      "roleAssignmentType": "string",
      "entityName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rowUID` | string |  |
| `createdDtm` | string |  |
| `updatedDtm` | string |  |
| `changeToken` | string |  |
| `userContactNumber` | string |  |
| `userContactType` | string |  |
| `inviteSent` | number |  |
| `fullName` | string |  |
| `userContactPhoto` | string |  |
| `language` | string |  |
| `uIMode` | string |  |
| `isEnabled` | number |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `gender` | string |  |
| `birthDate` | string |  |
| `homeAddress` | string |  |
| `homeCity` | string |  |
| `homeState` | string |  |
| `homeZip` | string |  |
| `phoneNumber` | string |  |
| `businessEntity` | string |  |
| `position` | string |  |
| `employer` | string |  |
| `supervisor` | string |  |
| `employeeID` | string |  |
| `hireDate` | string |  |
| `positionStartDate` | string |  |
| `industryStartDate` | string |  |
| `authProvider` | string |  |
| `username` | string |  |
| `emailAddress` | string |  |
| `mobilePhoneNumber` | string |  |
| `roleAssignmentType` | string |  |
| `entityName` | string |  |

## Native endpoint

Through the native EHS Insight API, this operation is `GET /v6/entity/UserContact/list?:customparams` (base URL `https://{{credentials.companyName}}.ehsinsight.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-contacts.md) for the provider-specific parameters and requirements.

