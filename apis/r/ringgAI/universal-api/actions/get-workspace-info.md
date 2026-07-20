# Ringg AI: Get Workspace Info

Retrieves workspace information from Ringg AI.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-workspace-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-workspace-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-workspace-info?${params}`, {
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
      "workspaceInfo": {
        "apiKey": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "credits": 1,
        "id": "string",
        "lockedCredits": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `workspaceInfo` | object |  |
| `workspaceInfo.apiKey` | string |  |
| `workspaceInfo.createdAt` | date |  |
| `workspaceInfo.credits` | number |  |
| `workspaceInfo.id` | string |  |
| `workspaceInfo.lockedCredits` | number |  |
| `workspaceInfo.name` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `GET /workspace` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-info.md) for the provider-specific parameters and requirements.

