# Planning Center: Create Person

Creates a new person in Planning Center.

```
POST https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planning Center `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/create-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | JSON:API resource object containing the Person type, attributes, and optional relationships. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no |  |

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

Through the native Planning Center API, this operation is `POST /people/v2/people` (base URL `https://api.planningcenteronline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.

