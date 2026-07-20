# Convex: Get Deployment

Retrieves a Convex deployment by name.

```
GET https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-deployment?connectionId=$CONNECTION_ID&deploymentName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deploymentName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-deployment?${params}`, {
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
| `deploymentName` | string | yes | The Convex deployment name. |

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

Through the native Convex API, this operation is `GET /deployments/:deployment_name` (base URL `https://api.convex.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment.md) for the provider-specific parameters and requirements.

