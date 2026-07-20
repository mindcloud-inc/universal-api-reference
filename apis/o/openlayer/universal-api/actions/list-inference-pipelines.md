# Openlayer: List Inference Pipelines

Retrieves inference pipelines for a project in Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-inference-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-inference-pipelines?connectionId=$CONNECTION_ID&projectId=2fcd0a42-23a7-44bb-b4fa-4fc3168fe248" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "2fcd0a42-23a7-44bb-b4fa-4fc3168fe248"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-inference-pipelines?${params}`, {
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
| `projectId` | string | yes | Openlayer project ID. Default: `2fcd0a42-23a7-44bb-b4fa-4fc3168fe248`. |

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
          "links": {
            "app": "https://example.com"
          },
          "name": "Ava Chen",
          "projectId": "string",
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
| `items[].dateUpdated` | string |  |
| `items[].description` | string |  |
| `items[].id` | string |  |
| `items[].links.app` | string |  |
| `items[].name` | string |  |
| `items[].projectId` | string |  |
| `items[].status` | string |  |
| `items[].workspaceId` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /projects/:projectId/inference-pipelines` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inference-pipelines.md) for the provider-specific parameters and requirements.

