# Mural: List Default and Custom Templates for Workspace

Finds default and custom templates in Mural for a workspace.

```
GET https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-default-and-custom-templates-for-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-default-and-custom-templates-for-workspace?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-default-and-custom-templates-for-workspace?${params}`, {
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
| `withoutDefault` | boolean | no | Exclude default templates when true. |
| `workspaceId` | string | yes | Unique identifier of a workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdOn": 1,
      "description": "string",
      "id": "string",
      "muralId": "string",
      "name": "Ava Chen",
      "thumbUrl": "https://example.com",
      "type": "string",
      "updatedBy": "string",
      "updatedOn": 1,
      "viewLink": "https://example.com",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string |  |
| `createdOn` | number |  |
| `description` | string |  |
| `id` | string |  |
| `muralId` | string |  |
| `name` | string |  |
| `thumbUrl` | string |  |
| `type` | string |  |
| `updatedBy` | string |  |
| `updatedOn` | number |  |
| `viewLink` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Mural API, this operation is `GET /workspaces/:workspaceId/templates` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-default-and-custom-templates-for-workspace.md) for the provider-specific parameters and requirements.

