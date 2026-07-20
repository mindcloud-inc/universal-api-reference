# Planning Center: List Household People

Retrieves people in a household from Planning Center.

```
GET https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-household-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planning Center `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-household-people?connectionId=$CONNECTION_ID&limit=25&offset=0&householdId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "householdId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-household-people?${params}`, {
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
| `householdId` | string | yes | The household id. |
| `nonPending` | string | no | Filter household people by non_pending. |
| `withoutDeceased` | string | no | Filter household people by without_deceased. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "accountingAdministrator": true,
        "anniversary": "2026-05-07T12:00:00.000Z",
        "avatar": "string",
        "birthdate": "2026-05-07T12:00:00.000Z",
        "canCreateForms": true,
        "canEmailLists": true,
        "child": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "demographicAvatarUrl": "https://example.com",
        "directoryStatus": "string",
        "firstName": "Ava",
        "gender": "string",
        "givenName": "Ava Chen",
        "grade": 1,
        "graduationYear": 1,
        "inactivatedAt": "2026-05-07T12:00:00.000Z",
        "lastName": "Chen",
        "loginIdentifier": "string",
        "medicalNotes": "string",
        "membership": "string",
        "mfaConfigured": true,
        "middleName": "Ava Chen",
        "name": "Ava Chen",
        "nickname": "Ava Chen",
        "passedBackgroundCheck": true,
        "peoplePermissions": "string",
        "remoteId": 1,
        "resourcePermissionFlags": {
          "canAccessWorkflows": true
        },
        "schoolType": "string",
        "siteAdministrator": true,
        "status": "string",
        "stripeCustomerIdentifier": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.accountingAdministrator` | boolean |  |
| `attributes.anniversary` | date |  |
| `attributes.avatar` | string |  |
| `attributes.birthdate` | date |  |
| `attributes.canCreateForms` | boolean |  |
| `attributes.canEmailLists` | boolean |  |
| `attributes.child` | boolean |  |
| `attributes.createdAt` | date |  |
| `attributes.demographicAvatarUrl` | string |  |
| `attributes.directoryStatus` | string |  |
| `attributes.firstName` | string |  |
| `attributes.gender` | string |  |
| `attributes.givenName` | string |  |
| `attributes.grade` | number |  |
| `attributes.graduationYear` | number |  |
| `attributes.inactivatedAt` | date |  |
| `attributes.lastName` | string |  |
| `attributes.loginIdentifier` | string |  |
| `attributes.medicalNotes` | string |  |
| `attributes.membership` | string |  |
| `attributes.mfaConfigured` | boolean |  |
| `attributes.middleName` | string |  |
| `attributes.name` | string |  |
| `attributes.nickname` | string |  |
| `attributes.passedBackgroundCheck` | boolean |  |
| `attributes.peoplePermissions` | string |  |
| `attributes.remoteId` | number |  |
| `attributes.resourcePermissionFlags.canAccessWorkflows` | boolean |  |
| `attributes.schoolType` | string |  |
| `attributes.siteAdministrator` | boolean |  |
| `attributes.status` | string |  |
| `attributes.stripeCustomerIdentifier` | string |  |
| `attributes.updatedAt` | date |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Planning Center API, this operation is `GET /people/v2/households/:household_id/people` (base URL `https://api.planningcenteronline.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-household-people.md) for the provider-specific parameters and requirements.

