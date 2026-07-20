# Clarifai: Update Workflow

Updates an existing workflow in Clarifai.

```
PATCH https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PATCH "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-workflow', {
  method: 'PATCH',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | no | Clarifai app ID. |

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

Through the native Clarifai API, this operation is `PATCH /v2/users/{{credentials.userId}}/apps/{{appId}}/workflows` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workflow.md) for the provider-specific parameters and requirements.

