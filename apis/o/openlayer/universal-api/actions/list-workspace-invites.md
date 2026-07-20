# Openlayer: List Workspace Invites

Retrieves invites for a workspace in Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-workspace-invites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-workspace-invites?connectionId=$CONNECTION_ID&workspaceId=b9ef2789-e1dd-4946-9ab0-189dcee20750" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "b9ef2789-e1dd-4946-9ab0-189dcee20750"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-workspace-invites?${params}`, {
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
| `workspaceId` | string | yes | Openlayer workspace ID. Default: `b9ef2789-e1dd-4946-9ab0-189dcee20750`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_meta": {
        "page": 1,
        "perPage": 1,
        "totalItems": 1,
        "totalPages": 1
      },
      "items": [
        {
          "dateCreated": "string",
          "email": "ava@example.com",
          "id": "string",
          "status": "string",
          "workspaceId": "string"
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
| `_meta.page` | number |  |
| `_meta.perPage` | number |  |
| `_meta.totalItems` | number |  |
| `_meta.totalPages` | number |  |
| `items[].dateCreated` | string |  |
| `items[].email` | string |  |
| `items[].id` | string |  |
| `items[].status` | string |  |
| `items[].workspaceId` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /workspaces/:workspaceId/invites` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-invites.md) for the provider-specific parameters and requirements.

