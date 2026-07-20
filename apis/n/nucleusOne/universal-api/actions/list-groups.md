# Nucleus One: List Groups

Retrieves project groups from Nucleus One.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-groups?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId&projectId=Enter%20projectId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId",
  "projectId": "Enter projectId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-groups?${params}`, {
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
| `organizationId` | string | yes | Organization ID Example: `Enter organizationId`. |
| `projectId` | string | yes | Project ID Example: `Enter projectId`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Pagination cursor. Leave empty to get the first page of results. Example: `Paste a cursor from a previous response`. |
| `getAll` | string | no | Get all results without pagination Example: `Enter getAll`. |
| `sortDescending` | string | no | Sort results in descending order Example: `Enter sortDescending`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$schema": "string",
      "CreatedByUserEmail": "ava@example.com",
      "CreatedByUserID": "string",
      "CreatedByUserName": "Ava Chen",
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "ID": "string",
      "ModifiedOn": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "NameLower": "Ava Chen",
      "OrganizationID": "string",
      "OrganizationName": "Ava Chen",
      "ProjectAccess": {},
      "ProjectID": "string",
      "ProjectIsDisabled": true,
      "ProjectName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `CreatedByUserEmail` | string |  |
| `CreatedByUserID` | string |  |
| `CreatedByUserName` | string |  |
| `CreatedOn` | date |  |
| `ID` | string |  |
| `ModifiedOn` | date |  |
| `Name` | string |  |
| `NameLower` | string |  |
| `OrganizationID` | string |  |
| `OrganizationName` | string |  |
| `ProjectAccess` | object |  |
| `ProjectID` | string |  |
| `ProjectIsDisabled` | boolean |  |
| `ProjectName` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projects/:projectId/groups` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

