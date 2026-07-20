# Shuffll: List Workspace Templates

Retrieves workspace templates from Shuffll.

```
GET https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-workspace-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-workspace-templates?connectionId=$CONNECTION_ID&organizationId=69cac8104c4a701fd26271a1&workspaceId=69cac8104c4a701fd26271a5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "69cac8104c4a701fd26271a1",
  "workspaceId": "69cac8104c4a701fd26271a5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-workspace-templates?${params}`, {
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
| `organizationId` | string | yes | Shuffll organization id. Default: `69cac8104c4a701fd26271a1`. |
| `workspaceId` | string | yes | Shuffll workspace id. Default: `69cac8104c4a701fd26271a5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Template description. |
| `id` | string | Template id. |
| `name` | string | Template name. |

## Native endpoint

Through the native Shuffll API, this operation is `GET /auth/organization/:organizationId/workspace/:workspaceId/templates` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-templates.md) for the provider-specific parameters and requirements.

