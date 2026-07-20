# Nucleus One: List Project Members

Retrieves project members from Nucleus One.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-project-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-project-members?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId&projectId=Enter%20projectId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId",
  "projectId": "Enter projectId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-project-members?${params}`, {
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
| `organizationId` | string | yes | organizationId path parameter. Example: `Enter organizationId`. |
| `projectId` | string | yes | projectId path parameter. Example: `Enter projectId`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Pagination cursor. Leave empty to get the first page of results. Example: `Paste a cursor from a previous response`. |
| `getAll` | string | no | If true, returns all results without pagination. Example: `Enter getAll`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$schema": "string",
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "Disabled": true,
      "ID": "string",
      "IsAdmin": true,
      "IsReadOnly": true,
      "IsStakeholder": true,
      "OrganizationID": "string",
      "OrganizationMemberID": "string",
      "OrganizationMemberIsAdmin": true,
      "OrganizationName": "Ava Chen",
      "ProjectAccess": {},
      "ProjectID": "string",
      "ProjectIsDisabled": true,
      "ProjectName": "Ava Chen",
      "UserEmail": "ava@example.com",
      "UserID": "string",
      "UserName": "Ava Chen",
      "UserNameLower": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `CreatedOn` | date |  |
| `Disabled` | boolean |  |
| `ID` | string |  |
| `IsAdmin` | boolean |  |
| `IsReadOnly` | boolean |  |
| `IsStakeholder` | boolean |  |
| `OrganizationID` | string |  |
| `OrganizationMemberID` | string |  |
| `OrganizationMemberIsAdmin` | boolean |  |
| `OrganizationName` | string |  |
| `ProjectAccess` | object |  |
| `ProjectID` | string |  |
| `ProjectIsDisabled` | boolean |  |
| `ProjectName` | string |  |
| `UserEmail` | string |  |
| `UserID` | string |  |
| `UserName` | string |  |
| `UserNameLower` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projects/:projectId/members` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-members.md) for the provider-specific parameters and requirements.

