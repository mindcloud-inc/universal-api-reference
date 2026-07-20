# Teamhood: List Workspace Boards

Retrieves boards for a Teamhood workspace.

```
GET https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-workspace-boards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamhood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-workspace-boards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-workspace-boards?${params}`, {
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
| `workspaceId` | string | no | The Teamhood workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "boards": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boards` | array<object> | Boards in the requested Teamhood workspace. |

## Native endpoint

Through the native Teamhood API, this operation is `GET /workspaces/:workspaceId/boards` (base URL `https://api-mindcloud1.teamhood.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-boards.md) for the provider-specific parameters and requirements.

