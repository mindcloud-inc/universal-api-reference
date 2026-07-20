# Elastic Cloud: Shut Down Deployment

Shuts down a deployment in Elastic Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/shutdown-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/shutdown-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deploymentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/shutdown-deployment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deploymentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deploymentId` | string | yes | Identifier for the deployment. |
| `hide` | boolean | no | Hide the deployment while shutting it down. Only applies to platform administrators. |
| `skipSnapshot` | boolean | no | Skip snapshots before shutting down the deployment resources. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Elastic Cloud API returns.

## Native endpoint

Through the native Elastic Cloud API, this operation is `POST /deployments/:deployment_id/_shutdown` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/shutdown-deployment.md) for the provider-specific parameters and requirements.

