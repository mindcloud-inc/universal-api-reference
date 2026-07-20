# Vercel: Create Deployment

Creates a new deployment in Vercel.

```
POST https://connect.mindcloud.co/v1/universal/vercel/latest/actions/create-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/create-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deploymentId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vercel/latest/actions/create-deployment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deploymentId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deploymentId` | string | yes | An existing deployment id to redeploy. |
| `name` | string | yes | The project name used in the deployment URL. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `withLatestCommit` | boolean | no | Force the latest commit when redeploying an existing deployment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "readyState": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `id` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `readyState` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Vercel API, this operation is `POST /v13/deployments` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deployment.md) for the provider-specific parameters and requirements.

