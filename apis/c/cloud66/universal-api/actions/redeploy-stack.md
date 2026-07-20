# Cloud 66: Redeploy Stack

Redeploys a stack in your Cloud 66 account.

```
POST https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/redeploy-stack
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud 66 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/redeploy-stack" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stackId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/redeploy-stack', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stackId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stackId` | string | yes | The stack UID. |
| `gitRef` | string | no | Git reference to redeploy for non-docker stacks. |
| `services` | string | no | Docker service:image_tag pairs to deploy. |
| `deploymentProfile` | string | no | Deployment profile name. |
| `userReference` | string | no | Metadata reference to attach to the stack action. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloud 66 API returns.

## Native endpoint

Through the native Cloud 66 API, this operation is `POST /stacks/:stack_id/deployments` (base URL `https://app.cloud66.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/redeploy-stack.md) for the provider-specific parameters and requirements.

