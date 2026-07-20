# ProProfs Project: Create Project

Creates a new project in ProProfs Project.

```
POST https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | The project description. |
| `projectName` | string | yes | The project name. |

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

Through the native ProProfs Project API, this operation is `POST /projects` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

