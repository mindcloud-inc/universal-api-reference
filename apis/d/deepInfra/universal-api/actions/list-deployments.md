# Deep Infra: List Deployments



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-deployments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-deployments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-deployments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "deploy_id": "string",
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
| `model_name` | string | Model deployed. |
| `name` | string | Deployment name. |
| `status` | string | Deployment status. |
| `updated_at` | string | Last deployment update timestamp. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /deploy/list` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deployments.md) for the provider-specific parameters and requirements.

