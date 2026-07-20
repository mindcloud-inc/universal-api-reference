# Openlayer: List Project Goals

Retrieves goals for a project in Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-project-goals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-project-goals?connectionId=$CONNECTION_ID&projectId=2fcd0a42-23a7-44bb-b4fa-4fc3168fe248&workspaceId=b9ef2789-e1dd-4946-9ab0-189dcee20750" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "2fcd0a42-23a7-44bb-b4fa-4fc3168fe248",
  "workspaceId": "b9ef2789-e1dd-4946-9ab0-189dcee20750"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-project-goals?${params}`, {
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
| `projectId` | string | yes | The Openlayer project ID. Default: `2fcd0a42-23a7-44bb-b4fa-4fc3168fe248`. |
| `workspaceId` | string | yes | Workspace context required by Openlayer for project goal listing. Default: `b9ef2789-e1dd-4946-9ab0-189dcee20750`. |

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
          "id": "string",
          "name": "Ava Chen",
          "priority": "string",
          "projectId": "string",
          "subtype": "string",
          "type": "string"
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
| `items[].id` | string |  |
| `items[].name` | string |  |
| `items[].priority` | string |  |
| `items[].projectId` | string |  |
| `items[].subtype` | string |  |
| `items[].type` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /projects/:projectId/goals` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-goals.md) for the provider-specific parameters and requirements.

