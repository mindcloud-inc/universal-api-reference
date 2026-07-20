# Typebot: List Workspace Members



```
GET https://connect.mindcloud.co/v1/universal/typebot/latest/actions/list-workspace-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typebot/latest/actions/list-workspace-members?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typebot/latest/actions/list-workspace-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | Workspace ID to list members for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "role": "string",
      "user": {
        "email": "ava@example.com"
      },
      "userId": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `role` | string |  |
| `user.email` | string |  |
| `userId` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Typebot API, this operation is `GET /v1/workspaces/:workspaceId/members` (base URL `https://app.typebot.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-members.md) for the provider-specific parameters and requirements.

