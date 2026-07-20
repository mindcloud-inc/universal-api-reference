# Elastic Cloud: Update Deployment

Updates an existing deployment in Elastic Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/update-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/update-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "deploymentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/update-deployment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "deploymentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | The deployment definition to apply. |
| `deploymentId` | string | yes | Identifier for the deployment. |
| `hidePrunedOrphans` | boolean | no | Hide orphaned resources that were shut down when pruning is enabled. |
| `skipSnapshot` | boolean | no | Skip snapshots before shutting down orphaned resources when pruning is enabled. |
| `validateOnly` | boolean | no | Validate the deployment update without applying it. |
| `version` | string | no | Resource version to use for conflict checks during the update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "settings": {
        "autoOps": {
          "status": "string"
        },
        "autoscalingEnabled": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `settings.autoOps.status` | string |  |
| `settings.autoscalingEnabled` | boolean |  |

## Native endpoint

Through the native Elastic Cloud API, this operation is `PUT /deployments/:deployment_id` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deployment.md) for the provider-specific parameters and requirements.

