# Damstra Forms: List Users

Retrieves users from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-users?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | string | no | Active state (true = Active, false = Inactive, all = All). One of: `0`, `1`, `2`. Default: `true`. Example: `true`. |
| `updatedFrom` | string | no | Only return results updated after the specified value. It will try to make sense of whatever datetime format you provide, but the example shows the officially supported format. Example: `2016-12-31T13:50:00Z`. |
| `showManaged` | boolean | no | Show/hide the managed attribute. Default: `false`. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "canCreateProjects": true,
      "canEditManagedTemplates": true,
      "canExport": true,
      "canManageAllProjects": true,
      "canManageCompanies": true,
      "canManageInsights": true,
      "canManageOrganisation": true,
      "canManageTemplates": true,
      "canManageUsers": true,
      "canViewDiagnostics": true,
      "confirmed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "damstraId": "string",
      "department": "string",
      "email": "ava@example.com",
      "href": "string",
      "id": 1,
      "jobTitle": "string",
      "lockVersion": 1,
      "managed": true,
      "name": "Ava Chen",
      "type": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userType": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | From Damstra Forms API example response. |
| `canCreateProjects` | boolean | From Damstra Forms API example response. |
| `canEditManagedTemplates` | boolean | From Damstra Forms API example response. |
| `canExport` | boolean | From Damstra Forms API example response. |
| `canManageAllProjects` | boolean | From Damstra Forms API example response. |
| `canManageCompanies` | boolean | From Damstra Forms API example response. |
| `canManageInsights` | boolean | From Damstra Forms API example response. |
| `canManageOrganisation` | boolean | From Damstra Forms API example response. |
| `canManageTemplates` | boolean | From Damstra Forms API example response. |
| `canManageUsers` | boolean | From Damstra Forms API example response. |
| `canViewDiagnostics` | boolean | From Damstra Forms API example response. |
| `confirmed` | boolean | From Damstra Forms API example response. |
| `createdAt` | date | From Damstra Forms API example response. |
| `damstraId` | string | From Damstra Forms API example response. |
| `department` | string | From Damstra Forms API example response. |
| `email` | string | From Damstra Forms API example response. |
| `href` | string | From Damstra Forms API example response. |
| `id` | number | From Damstra Forms API example response. |
| `jobTitle` | string | From Damstra Forms API example response. |
| `lockVersion` | number | From Damstra Forms API example response. |
| `managed` | boolean | From Damstra Forms API example response. |
| `name` | string | From Damstra Forms API example response. |
| `type` | number | From Damstra Forms API example response. |
| `updatedAt` | date | From Damstra Forms API example response. |
| `userType` | string | From Damstra Forms API example response. |
| `uuid` | string | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /users` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

