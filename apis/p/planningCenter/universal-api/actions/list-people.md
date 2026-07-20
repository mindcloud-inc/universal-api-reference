# Planning Center: List People

Retrieves people from Planning Center.

```
GET https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planning Center `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-people?${params}`, {
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
| `where.accountingAdministrator` | boolean | no |  |
| `where.anniversary` | date | no |  |
| `where.birthdate` | date | no |  |
| `where.child` | boolean | no |  |
| `where.createdAt` | date | no |  |
| `where.firstName` | string | no |  |
| `where.gender` | string | no |  |
| `where.givenName` | string | no |  |
| `where.grade` | number | no |  |
| `where.graduationYear` | number | no |  |
| `where.id` | string | no |  |
| `where.inactivatedAt` | date | no |  |
| `where.lastName` | string | no |  |
| `where.medicalNotes` | string | no |  |
| `where.membership` | string | no |  |
| `where.mfaConfigured` | boolean | no |  |
| `where.middleName` | string | no |  |
| `where.nickname` | string | no |  |
| `where.peoplePermissions` | string | no |  |
| `where.primaryCampusId` | number | no |  |
| `where.remoteId` | number | no |  |
| `where.searchName` | string | no |  |
| `where.searchNameOrEmail` | string | no |  |
| `where.searchNameOrEmailOrPhoneNumber` | string | no |  |
| `where.searchPhoneNumber` | string | no |  |
| `where.searchPhoneNumberE164` | string | no |  |
| `where.siteAdministrator` | boolean | no |  |
| `where.status` | string | no |  |
| `where.updatedAt` | date | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Include associated resources in the response. |
| `order` | string | no | Sort the returned people; prefix the field with a hyphen for descending order. |
| `filter` | string | no |  |

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

Through the native Planning Center API, this operation is `GET /people/v2/people` (base URL `https://api.planningcenteronline.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

