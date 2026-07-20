# Clockify: List User Groups

Lists all user groups in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-user-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-user-groups?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-user-groups?${params}`, {
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
| `includeTeamManagers` | boolean | no |  |
| `name` | string | no |  |
| `page` | number | no |  |
| `pageSize` | number | no |  |
| `projectId` | string | no |  |
| `sortColumn` | list | no | One of: `ID`, `NAME`. |
| `sortOrder` | list | no | One of: `ASCENDING`, `DESCENDING`. |
| `workspaceId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array<object> |  |
| `items[].id` | string |  |
| `items[].name` | string |  |
| `items[].teamManagers[]` | array<object> |  |
| `items[].teamManagers[].id` | string |  |
| `items[].teamManagers[].name` | string |  |
| `items[].userIds[]` | array<string> |  |
| `items[].workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/user-groups` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-groups.md) for the provider-specific parameters and requirements.

