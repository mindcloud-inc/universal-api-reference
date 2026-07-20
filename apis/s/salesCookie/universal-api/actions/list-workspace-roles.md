# Sales Cookie: List Workspace Roles

Retrieves workspace roles from Sales Cookie.

```
GET https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-workspace-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-workspace-roles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-workspace-roles?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLevel": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "createdById": "string",
      "csvFormatting": "string",
      "currency": "string",
      "customProperties": "string",
      "dashboardDisabled": true,
      "dateFormatting": "string",
      "directManagerId": "string",
      "endDate": "string",
      "id": "string",
      "isDeleted": true,
      "isOnboarded": true,
      "isPending": true,
      "loggedIn": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "planStartEndDatesXml": "string",
      "preferShortDates": true,
      "prevAccessLevel": "string",
      "startDate": "string",
      "systemUserId": "string",
      "tag": "string",
      "tags": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "updatedById": "string",
      "useWorkspaceTimeZone": true,
      "viewAnnouncementsDate": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | string |  |
| `created` | date |  |
| `createdById` | string |  |
| `csvFormatting` | string |  |
| `currency` | string |  |
| `customProperties` | string |  |
| `dashboardDisabled` | boolean |  |
| `dateFormatting` | string |  |
| `directManagerId` | string |  |
| `endDate` | string |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `isOnboarded` | boolean |  |
| `isPending` | boolean |  |
| `loggedIn` | date |  |
| `notes` | string |  |
| `planStartEndDatesXml` | string |  |
| `preferShortDates` | boolean |  |
| `prevAccessLevel` | string |  |
| `startDate` | string |  |
| `systemUserId` | string |  |
| `tag` | string |  |
| `tags` | string |  |
| `updated` | date |  |
| `updatedById` | string |  |
| `useWorkspaceTimeZone` | boolean |  |
| `viewAnnouncementsDate` | date |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Sales Cookie API, this operation is `GET /odata/:apiKey/WorkspaceRole` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workspace-roles.md) for the provider-specific parameters and requirements.

