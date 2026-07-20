# v0: Create Deployment

Creates a new deployment in v0.

```
POST https://connect.mindcloud.co/v1/universal/v0/latest/actions/create-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/v0/latest/actions/create-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "chatId": "string",
  "versionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/v0/latest/actions/create-deployment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "chatId": "string",
    "versionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The project that owns the deployment. |
| `chatId` | string | yes | The chat to deploy. |
| `versionId` | string | yes | The chat version to deploy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": "https://example.com",
      "chatId": "string",
      "id": "string",
      "inspectorUrl": "https://example.com",
      "object": "string",
      "projectId": "string",
      "versionId": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUrl` | string |  |
| `chatId` | string |  |
| `id` | string |  |
| `inspectorUrl` | string |  |
| `object` | string |  |
| `projectId` | string |  |
| `versionId` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native v0 API, this operation is `POST /v1/deployments` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deployment.md) for the provider-specific parameters and requirements.

