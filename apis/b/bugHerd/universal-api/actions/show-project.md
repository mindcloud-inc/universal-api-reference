# BugHerd: Show Project

Retrieves a project from BugHerd.

```
GET https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/show-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/show-project?connectionId=$CONNECTION_ID&project_id=511891" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "511891"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/show-project?${params}`, {
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
| `project_id` | number | yes | Example: `511891`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowGuestsChangeTaskStatus": true,
      "allowProjectOwnerNotifications": true,
      "allowProjectSummaryEmail": true,
      "allowTaskDoneEmail": true,
      "apiKey": "string",
      "assignGuests": true,
      "changeGuestDefaultColumn": true,
      "columns": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "name": "Ava Chen",
          "projectId": 1,
          "tasksCount": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "devurl": "https://example.com",
      "guests": [
        {
          "avatarUrl": "https://example.com",
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "id": 1
        }
      ],
      "guestsSeeGuests": true,
      "id": 1,
      "isActive": true,
      "isPublic": true,
      "members": [
        {
          "avatarUrl": "https://example.com",
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "id": 1
        }
      ],
      "name": "Ava Chen",
      "ownerName": "Ava Chen",
      "sites": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowGuestsChangeTaskStatus` | boolean |  |
| `allowProjectOwnerNotifications` | boolean |  |
| `allowProjectSummaryEmail` | boolean |  |
| `allowTaskDoneEmail` | boolean |  |
| `apiKey` | string |  |
| `assignGuests` | boolean |  |
| `changeGuestDefaultColumn` | boolean |  |
| `columns[].createdAt` | date |  |
| `columns[].id` | number |  |
| `columns[].name` | string |  |
| `columns[].projectId` | number |  |
| `columns[].tasksCount` | number |  |
| `columns[].updatedAt` | date |  |
| `devurl` | string |  |
| `guests[].avatarUrl` | string |  |
| `guests[].displayName` | string |  |
| `guests[].email` | string |  |
| `guests[].id` | number |  |
| `guestsSeeGuests` | boolean |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isPublic` | boolean |  |
| `members[].avatarUrl` | string |  |
| `members[].displayName` | string |  |
| `members[].email` | string |  |
| `members[].id` | number |  |
| `name` | string |  |
| `ownerName` | string |  |
| `sites[]` | string |  |

## Native endpoint

Through the native BugHerd API, this operation is `GET projects/:project_id.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-project.md) for the provider-specific parameters and requirements.

