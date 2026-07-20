# Vercel: Get Deployment

Retrieves a deployment record from Vercel.

```
GET https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-deployment?connectionId=$CONNECTION_ID&idOrUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-deployment?${params}`, {
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
| `idOrUrl` | string | yes | The unique identifier or hostname of the deployment. |
| `withGitRepoInfo` | string | no | Whether to add in gitRepo information. |

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

Through the native Vercel API, this operation is `GET /v13/deployments/:idOrUrl` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment.md) for the provider-specific parameters and requirements.

