# Convex: Create Deployment

Creates a new deployment in Convex.

```
POST https://connect.mindcloud.co/v1/universal/convex/latest/actions/create-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/convex/latest/actions/create-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/convex/latest/actions/create-deployment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The Convex project ID. |
| `type` | string | yes | The deployment type to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "class": "string",
      "createTime": 1,
      "creator": 1,
      "dashboardEditConfirmation": "string",
      "deploymentType": "string",
      "deploymentUrl": "https://example.com",
      "id": 1,
      "isDefault": true,
      "kind": "string",
      "name": "Ava Chen",
      "previewIdentifier": "string",
      "projectId": 1,
      "reference": "string",
      "region": "string",
      "sendLogsToClient": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `class` | string |  |
| `createTime` | number |  |
| `creator` | number |  |
| `dashboardEditConfirmation` | string |  |
| `deploymentType` | string |  |
| `deploymentUrl` | string |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `kind` | string |  |
| `name` | string |  |
| `previewIdentifier` | string |  |
| `projectId` | number |  |
| `reference` | string |  |
| `region` | string |  |
| `sendLogsToClient` | boolean |  |

## Native endpoint

Through the native Convex API, this operation is `POST /projects/:project_id/create_deployment` (base URL `https://api.convex.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deployment.md) for the provider-specific parameters and requirements.

