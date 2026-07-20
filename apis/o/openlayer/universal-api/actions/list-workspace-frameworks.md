# Openlayer: List Workspace Frameworks

Retrieves frameworks for a workspace in Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-workspace-frameworks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-workspace-frameworks?connectionId=$CONNECTION_ID&workspaceId=b9ef2789-e1dd-4946-9ab0-189dcee20750" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "b9ef2789-e1dd-4946-9ab0-189dcee20750"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-workspace-frameworks?${params}`, {
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
          "dateUpdated": "string",
          "description": "string",
          "enabled": true,
          "href": "string",
          "id": "string",
          "name": "Ava Chen",
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
| `items[].dateUpdated` | string |  |
| `items[].description` | string |  |
| `items[].enabled` | boolean |  |
| `items[].href` | string |  |
| `items[].id` | string |  |
| `items[].name` | string |  |
| `items[].workspaceId` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /workspaces/:workspaceId/frameworks` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-frameworks.md) for the provider-specific parameters and requirements.

