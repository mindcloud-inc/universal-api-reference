# Elastic Cloud: Create Deployment

Creates a new deployment in Elastic Cloud.

```
POST https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/create-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/create-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/create-deployment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | The deployment definition to create. |
| `requestId` | string | no | Optional idempotency token for deployment creation requests. |
| `templateId` | string | no | Optional deployment template to use when creating the deployment. |
| `validateOnly` | boolean | no | Validate the deployment definition without creating the deployment. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Elastic Cloud API returns.

## Native endpoint

Through the native Elastic Cloud API, this operation is `POST /deployments` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deployment.md) for the provider-specific parameters and requirements.

