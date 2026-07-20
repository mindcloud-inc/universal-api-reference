# SectorFlow.AI: Update Workspace



```
PUT https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/update-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SectorFlow.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/update-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/update-workspace', {
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
| `name` | string | no | Workspace name. |
| `workspaceId` | string | no | The workspace UUID. |

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
      "created": "string",
      "id": "string",
      "models": [
        {}
      ],
      "name": "Ava Chen",
      "sharingType": "string",
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
| `created` | string |  |
| `id` | string |  |
| `models` | array<object> |  |
| `name` | string |  |
| `sharingType` | string |  |
| `systemProject` | boolean |  |

## Native endpoint

Through the native SectorFlow.AI API, this operation is `POST /workspaces/{workspaceId}` (base URL `https://platform.sectorflow.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace.md) for the provider-specific parameters and requirements.

