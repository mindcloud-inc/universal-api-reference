# Convex: Delete Deployment

Deletes an existing deployment from Convex.

```
DELETE https://connect.mindcloud.co/v1/universal/convex/latest/actions/delete-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/convex/latest/actions/delete-deployment?connectionId=$CONNECTION_ID&deploymentName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deploymentName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convex/latest/actions/delete-deployment?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Convex API returns.

## Native endpoint

Through the native Convex API, this operation is `POST /deployments/:deployment_name/delete` (base URL `https://api.convex.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-deployment.md) for the provider-specific parameters and requirements.

