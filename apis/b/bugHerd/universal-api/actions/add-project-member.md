# BugHerd: Add Project Member

Adds a member to a BugHerd project.

```
POST https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/add-project-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/add-project-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "511891",
  "user_id": "591329"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/add-project-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "511891",
    "user_id": "591329"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | number | yes | Example: `511891`. |
| `user_id` | number | yes | Example: `591329`. |

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
          "createdAt": "string",
          "id": 1,
          "name": "Ava Chen",
          "projectId": 1,
          "tasksCount": 1,
          "updatedAt": "string"
        }
      ],
      "devurl": "https://example.com",
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
      "ownerName": {},
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
| `columns[].createdAt` | string |  |
| `columns[].id` | number |  |
| `columns[].name` | string |  |
| `columns[].projectId` | number |  |
| `columns[].tasksCount` | number |  |
| `columns[].updatedAt` | string |  |
| `devurl` | string |  |
| `guestsSeeGuests` | boolean |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isPublic` | boolean |  |
| `members[].avatarUrl` | string |  |
| `members[].displayName` | string |  |
| `members[].email` | string |  |
| `members[].id` | number |  |
| `name` | string |  |
| `ownerName` | object |  |
| `sites[]` | string |  |

## Native endpoint

Through the native BugHerd API, this operation is `POST projects/:project_id/add_member.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-project-member.md) for the provider-specific parameters and requirements.

