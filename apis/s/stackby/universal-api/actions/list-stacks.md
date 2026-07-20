# Stackby: List Stacks

Retrieves stacks from a Stackby workspace.

```
GET https://connect.mindcloud.co/v1/universal/stackby/latest/actions/list-stacks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackby/latest/actions/list-stacks?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackby/latest/actions/list-stacks?${params}`, {
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
| `workspaceId` | string | yes | Workspace identifier from Stackby. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "list": [
        {}
      ],
      "workspaceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `list` | array<object> | Stacks in the workspace. |
| `workspaceName` | string | Workspace display name. |

## Native endpoint

Through the native Stackby API, this operation is `GET /v0/stacklist/{{workspaceId}}` (base URL `https://stackby.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stacks.md) for the provider-specific parameters and requirements.

