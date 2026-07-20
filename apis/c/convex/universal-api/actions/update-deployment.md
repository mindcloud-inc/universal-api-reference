# Convex: Update Deployment

Updates an existing deployment in Convex.

```
PUT https://connect.mindcloud.co/v1/universal/convex/latest/actions/update-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/convex/latest/actions/update-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deploymentName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/convex/latest/actions/update-deployment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deploymentName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deploymentName` | string | yes | The Convex deployment name. |
| `reference` | string | no | The deployment reference to set. |
| `sendLogsToClient` | boolean | no | Whether to send logs to the client. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Convex API returns.

## Native endpoint

Through the native Convex API, this operation is `PATCH /deployments/:deployment_name` (base URL `https://api.convex.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deployment.md) for the provider-specific parameters and requirements.

