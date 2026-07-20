# Airiam AI: List Workspaces

Retrieves a list of workspaces from Airiam AI.

```
GET https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airiam AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/list-workspaces?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "systemProject": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowChatModelChange` | boolean | Whether users can change the chat model. |
| `chatHistoryRetentionDays` | number | Chat history retention period in days. |
| `chatHistoryType` | string | Chat history storage mode. |
| `contextType` | string | Workspace context visibility type. |
| `created` | date | Workspace creation timestamp. |
| `id` | string | Workspace ID. |
| `models` | array<object> | Models configured for the workspace. |
| `name` | string | Workspace name. |
| `sharingType` | string | Workspace sharing type. |
| `systemProject` | boolean | Whether the workspace is a system project. |

## Native endpoint

Through the native Airiam AI API, this operation is `GET /api/v1/workspaces` (base URL `https://platform.sectorflow.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

