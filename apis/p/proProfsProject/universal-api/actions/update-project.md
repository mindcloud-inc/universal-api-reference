# ProProfs Project: Update Project

Updates an existing project in ProProfs Project.

```
PUT https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | The updated project description. |
| `projectId` | string | yes | The project ID to update. |
| `projectName` | string | no | The updated project name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": "string",
      "archived": "string",
      "billableHours": "string",
      "clientId": "string",
      "clientName": "Ava Chen",
      "closed": "string",
      "color": "string",
      "currency": "string",
      "dateCreated": "string",
      "dateModified": "string",
      "description": "string",
      "dueDate": "string",
      "estimatedHours": "string",
      "fixedPrice": "string",
      "hourlyRate": "https://example.com",
      "important": "string",
      "notes": "string",
      "notifications": "string",
      "ongoing": "string",
      "price": "string",
      "progress": "string",
      "projectId": "string",
      "projectName": "Ava Chen",
      "projectOrder": "string",
      "public": "string",
      "recurring": "string",
      "startDate": "string",
      "tags": "string",
      "teams": [
        {
          "teamId": "string",
          "teamName": "Ava Chen"
        }
      ],
      "template": "string",
      "trackedSeconds": "string",
      "uri": "string",
      "userId": "string",
      "users": [
        {
          "userId": "string",
          "userName": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string |  |
| `archived` | string |  |
| `billableHours` | string |  |
| `clientId` | string |  |
| `clientName` | string |  |
| `closed` | string |  |
| `color` | string |  |
| `currency` | string |  |
| `dateCreated` | string |  |
| `dateModified` | string |  |
| `description` | string |  |
| `dueDate` | string |  |
| `estimatedHours` | string |  |
| `fixedPrice` | string |  |
| `hourlyRate` | string |  |
| `important` | string |  |
| `notes` | string |  |
| `notifications` | string |  |
| `ongoing` | string |  |
| `price` | string |  |
| `progress` | string |  |
| `projectId` | string |  |
| `projectName` | string |  |
| `projectOrder` | string |  |
| `public` | string |  |
| `recurring` | string |  |
| `startDate` | string |  |
| `tags` | string |  |
| `teams[].teamId` | string |  |
| `teams[].teamName` | string |  |
| `template` | string |  |
| `trackedSeconds` | string |  |
| `uri` | string |  |
| `userId` | string |  |
| `users[].userId` | string |  |
| `users[].userName` | string |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `PUT /projects/{{project_id}}` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

