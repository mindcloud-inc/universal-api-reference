# Airiam AI: Update Workspace

Updates an existing workspace in Airiam AI.

```
PUT https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/update-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airiam AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/update-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/update-workspace', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | Workspace identifier. |
| `name` | string | no | Updated workspace name. |
| `description` | string | no | Updated workspace description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowChatModelChange": true,
      "chatHistoryRetentionDays": 1,
      "chatHistoryType": "string",
      "contextType": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "models": [
        {}
      ],
      "name": "Ava Chen",
      "sharingType": "string",
      "slug": "string",
      "systemProject": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowChatModelChange` | boolean |  |
| `chatHistoryRetentionDays` | number |  |
| `chatHistoryType` | string |  |
| `contextType` | string |  |
| `created` | date |  |
| `id` | string |  |
| `models` | array<object> |  |
| `name` | string |  |
| `sharingType` | string |  |
| `slug` | string |  |
| `systemProject` | boolean |  |

## Native endpoint

Through the native Airiam AI API, this operation is `POST /api/v1/workspaces/:workspaceId` (base URL `https://platform.sectorflow.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace.md) for the provider-specific parameters and requirements.

