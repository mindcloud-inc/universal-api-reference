# BugHerd: Create Project

Creates a new project in BugHerd.

```
POST https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project.name": "Project Alpha"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project.name": "Project Alpha"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | object | no |  |
| `project.name` | string | yes | Example: `Project Alpha`. |
| `project.devurl` | string | no | Example: `https://example.com`. |
| `project.is_active` | boolean | no |  |
| `project.is_public` | boolean | no |  |
| `project.guests_see_guests` | boolean | no |  |

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
| `name` | string |  |
| `ownerName` | object |  |
| `sites[]` | string |  |

## Native endpoint

Through the native BugHerd API, this operation is `POST projects.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

