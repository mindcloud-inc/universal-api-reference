# Asana: Update a workspace

Updates a workspace in Asana.

```
PUT https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/update-a-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/update-a-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "string",
  "workspaceGid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/update-a-workspace', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "string",
    "workspaceGid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | string | yes |  |
| `workspaceGid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailDomains": [
        "ava@example.com"
      ],
      "gid": "string",
      "isOrganization": true,
      "name": "Ava Chen",
      "resourceType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailDomains[]` | string |  |
| `gid` | string |  |
| `isOrganization` | boolean |  |
| `name` | string |  |
| `resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `PUT workspaces/:workspace_gid` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-workspace.md) for the provider-specific parameters and requirements.

