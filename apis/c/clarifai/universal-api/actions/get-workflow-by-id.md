# Clarifai: Get Workflow By ID

Retrieves a workflow from Clarifai.

```
GET https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/get-workflow-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/get-workflow-by-id?connectionId=$CONNECTION_ID&appId=string&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/get-workflow-by-id?${params}`, {
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
| `workflowId` | string | yes | Clarifai workflow ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "createdAt": "string",
      "id": "string",
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
| `id` | string |  |
| `modifiedAt` | string |  |
| `nodes[].id` | string |  |
| `nodes[].model.appId` | string |  |
| `nodes[].model.id` | string |  |
| `nodes[].model.modelTypeId` | string |  |
| `nodes[].model.modelVersion.id` | string |  |
| `nodes[].model.name` | string |  |
| `nodes[].model.userId` | string |  |
| `userId` | string |  |
| `version.id` | string |  |
| `visibility.gettable` | number |  |

## Native endpoint

Through the native Clarifai API, this operation is `GET /v2/users/me/apps/:appId/workflows/:workflowId` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-by-id.md) for the provider-specific parameters and requirements.

