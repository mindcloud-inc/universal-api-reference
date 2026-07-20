# Deep Infra: Get Deployment Status



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-deployment-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-deployment-status?connectionId=$CONNECTION_ID&deployId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deployId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-deployment-status?${params}`, {
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
| `deployId` | string | yes | Dedicated deployment identifier from the deployment URL path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "deploy_id": "string",
      "gpu": "string",
      "model_name": "Ava Chen",
      "name": "Ava Chen",
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Deployment creation timestamp. |
| `deploy_id` | string | Deployment identifier. |
| `gpu` | string | GPU type when returned. |
| `model_name` | string | Model deployed. |
| `name` | string | Deployment name. |
| `status` | string | Deployment status. |
| `updated_at` | string | Last deployment update timestamp. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /deploy/:deploy_id` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment-status.md) for the provider-specific parameters and requirements.

