# Endear: Create Task



```
POST https://connect.mindcloud.co/v1/universal/endear/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Endear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/endear/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.type": "string",
  "variables.title": "string",
  "variables.timeZone": "string",
  "variables.dueDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/endear/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.type": "string",
    "variables.title": "string",
    "variables.timeZone": "string",
    "variables.dueDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.localId` | string | no | Local Id for the Endear GraphQL operation. |
| `variables.idempotencyKey` | string | no | Idempotency Key for the Endear GraphQL operation. |
| `variables.type` | string | yes | Type for the Endear GraphQL operation. |
| `variables.title` | string | yes | Title for the Endear GraphQL operation. |
| `variables.descriptionHtml` | string | no | Description Html for the Endear GraphQL operation. |
| `variables.timeZone` | string | yes | Time Zone for the Endear GraphQL operation. |
| `variables.dueDate` | date | yes | Due Date for the Endear GraphQL operation. |
| `variables.expiresAt` | date | no | Expires At for the Endear GraphQL operation. |
| `variables.assignToTeamId` | string | no | Assign To Team Id for the Endear GraphQL operation. |
| `variables.assignToUserId` | string | no | Assign To User Id for the Endear GraphQL operation. |
| `variables.notifyAssignees` | boolean | no | Notify Assignees for the Endear GraphQL operation. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.autoAssignmentStrategy[]` | array<string> | no | Auto Assignment Strategy for the Endear GraphQL operation. |
| `variables.conditions[]` | array<object> | no | Conditions for the Endear GraphQL operation. |
| `variables.associations[]` | array<object> | no | Associations for the Endear GraphQL operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Endear API, this operation is `POST /graphql` (base URL `https://api.endearhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

