# Ringg AI: Get All User Workspaces

Retrieves user workspaces from Ringg AI.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-all-user-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-all-user-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-all-user-workspaces?${params}`, {
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
      "workspaces": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "credits": 1,
          "id": "string",
          "lockedCredits": 1,
          "name": "Ava Chen",
          "role": "string"
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
| `workspaces` | array<object> |  |
| `workspaces[].createdAt` | date |  |
| `workspaces[].credits` | number |  |
| `workspaces[].id` | string |  |
| `workspaces[].lockedCredits` | number |  |
| `workspaces[].name` | string |  |
| `workspaces[].role` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `GET /workspace/all` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-user-workspaces.md) for the provider-specific parameters and requirements.

