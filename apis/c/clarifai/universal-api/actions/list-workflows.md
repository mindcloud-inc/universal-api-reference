# Clarifai: List Workflows

Retrieves workflows from Clarifai.

```
GET https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-workflows?connectionId=$CONNECTION_ID&limit=25&offset=0&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-workflows?${params}`, {
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
| `appId` | string | yes | Clarifai app ID. |
| `search` | string | no | Search term for workflow ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "image": {
        "hosted": {
          "crossorigin": "string",
          "prefix": "string",
          "sizes": [
            "string"
          ],
          "suffix": "string"
        },
        "url": "https://example.com"
      },
      "modifiedAt": "string",
      "nodes": [
        {
          "id": "string",
          "model": {
            "appId": "string",
            "id": "string",
            "modelTypeId": "string",
            "modelVersion": {
              "id": "string"
            },
            "name": "Ava Chen",
            "userId": "string"
          }
        }
      ],
      "notes": "string",
      "userId": "string",
      "version": {
        "id": "string"
      },
      "visibility": {
        "gettable": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `image.hosted.crossorigin` | string |  |
| `image.hosted.prefix` | string |  |
| `image.hosted.sizes[]` | string |  |
| `image.hosted.suffix` | string |  |
| `image.url` | string |  |
| `modifiedAt` | string |  |
| `nodes[].id` | string |  |
| `nodes[].model.appId` | string |  |
| `nodes[].model.id` | string |  |
| `nodes[].model.modelTypeId` | string |  |
| `nodes[].model.modelVersion.id` | string |  |
| `nodes[].model.name` | string |  |
| `nodes[].model.userId` | string |  |
| `notes` | string |  |
| `userId` | string |  |
| `version.id` | string |  |
| `visibility.gettable` | number |  |

## Native endpoint

Through the native Clarifai API, this operation is `GET /v2/users/me/apps/:appId/workflows` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workflows.md) for the provider-specific parameters and requirements.

