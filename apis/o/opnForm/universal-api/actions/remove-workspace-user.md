# OpnForm: Remove Workspace User

Removes a user from an OpnForm workspace.

```
DELETE https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/remove-workspace-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpnForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/remove-workspace-user?connectionId=$CONNECTION_ID&workspaceId=1&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1",
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/remove-workspace-user?${params}`, {
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
| `workspaceId` | number | yes |  |
| `userId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native OpnForm API, this operation is `DELETE /open/workspaces/:workspaceId/users/:userId/remove` (base URL `https://api.opnform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-workspace-user.md) for the provider-specific parameters and requirements.

