# Convex: Get Project Deployment

Retrieves a deployment from a Convex project.

```
GET https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-project-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-project-deployment?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-project-deployment?${params}`, {
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
| `projectId` | number | yes | The Convex project ID. |
| `reference` | string | no | The deployment reference to fetch. |
| `defaultProd` | boolean | no | Fetch the default production deployment for the caller. |
| `defaultDev` | boolean | no | Fetch the default development deployment for the caller. |

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

Through the native Convex API, this operation is `GET /projects/:project_id/deployment` (base URL `https://api.convex.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-deployment.md) for the provider-specific parameters and requirements.

