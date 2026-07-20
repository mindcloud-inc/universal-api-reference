# Vercel: Get Deployment Events

Retrieves deployment events for a Vercel deployment.

```
GET https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-deployment-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-deployment-events?connectionId=$CONNECTION_ID&idOrUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-deployment-events?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "deploymentId": "string",
      "id": "string",
      "serial": "string",
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `deploymentId` | string |  |
| `id` | string |  |
| `serial` | string |  |
| `text` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Vercel API, this operation is `GET /v3/deployments/:idOrUrl/events` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment-events.md) for the provider-specific parameters and requirements.

