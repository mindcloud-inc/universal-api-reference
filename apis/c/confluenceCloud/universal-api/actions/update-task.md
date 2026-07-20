# Confluence: Update Task

Updates an existing task in Confluence.

```
PUT https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloudId": "string",
  "id": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloudId": "string",
    "id": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cloudId` | string | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | string | yes | ID of the task. |
| `status` | string | yes | Set the task to complete or incomplete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": {},
      "body": {},
      "completedAt": {},
      "completedBy": {},
      "createdAt": "string",
      "createdBy": "string",
      "dueAt": {},
      "id": "string",
      "localId": "string",
      "pageId": "string",
      "spaceId": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | object |  |
| `body` | object |  |
| `completedAt` | object |  |
| `completedBy` | object |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `dueAt` | object |  |
| `id` | string |  |
| `localId` | string |  |
| `pageId` | string |  |
| `spaceId` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Confluence API, this operation is `PUT /ex/confluence/:cloudId/wiki/api/v2/tasks/:id` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

