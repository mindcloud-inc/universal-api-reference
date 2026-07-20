# NocoDB: List Bases

Retrieves bases in a NocoDB workspace.

```
GET https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-bases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-bases?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-bases?${params}`, {
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
| `workspaceId` | string | yes | Workspace identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "meta": {},
      "title": "string",
      "updatedAt": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `meta` | object |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native NocoDB API, this operation is `GET /api/v3/meta/workspaces/:workspaceId/bases` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bases.md) for the provider-specific parameters and requirements.

