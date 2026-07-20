# Chatvolt AI: Create or Update Dispatch

Creates a dispatch in Chatvolt AI, or updates an existing one.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/dispatches-create
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/dispatches-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/dispatches-create', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Include the ID to update an existing dispatch. Omit to create a new one. |
| `name` | string | no | The name of the dispatch. |
| `status` | string | no | The status of the dispatch (e.g., 'draft', 'scheduled', 'sent'). |
| `agentId` | string | no | The ID of the agent responsible for the dispatch. |
| `crmScenarioId` | string | no | The ID of the CRM scenario associated with the dispatch. |
| `crmStepId` | string | no | The ID of the CRM step associated with the dispatch. |
| `scheduledAt` | string | no | The date and time the dispatch is scheduled to run. |
| `templateMessage` | string | no | The message template for the dispatch. |
| `interval` | number | no | The interval in minutes between sending messages for the dispatch. |
| `defaultAssigneeId` | string | no | The ID of the default assignee for conversations created by this dispatch. |
| `defaultStatus` | string | no | The default status for conversations created by this dispatch. |
| `contactListIds[]` | array<string> | no | An array of contact list IDs to associate with the dispatch. |
| `exclusionContactListIds[]` | array<string> | no | An array of contact list IDs to exclude from the dispatch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "createdAt": "string",
      "crmScenarioId": "string",
      "crmStepId": "string",
      "errorCount": 1,
      "id": "string",
      "interval": 1,
      "latestErrorMessage": "string",
      "name": "Ava Chen",
      "scheduledAt": "string",
      "sentCount": 1,
      "status": "string",
      "templateMessage": "string",
      "totalCount": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | AgentId. |
| `createdAt` | string | CreatedAt. |
| `crmScenarioId` | string | CrmScenarioId. |
| `crmStepId` | string | CrmStepId. |
| `errorCount` | number | ErrorCount. |
| `id` | string | Id. |
| `interval` | number | Interval. |
| `latestErrorMessage` | string | LatestErrorMessage. |
| `name` | string | Name. |
| `scheduledAt` | string | ScheduledAt. |
| `sentCount` | number | SentCount. |
| `status` | string | Status. |
| `templateMessage` | string | TemplateMessage. |
| `totalCount` | number | TotalCount. |
| `updatedAt` | string | UpdatedAt. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /dispatches` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/dispatches-create.md) for the provider-specific parameters and requirements.

