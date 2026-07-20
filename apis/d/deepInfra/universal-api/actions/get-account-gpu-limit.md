# Deep Infra: Get Account GPU Limit



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-account-gpu-limit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-account-gpu-limit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-account-gpu-limit?${params}`, {
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
      "available": 1,
      "gpu_limit": 1,
      "limit": 1,
      "used": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | number | Available GPUs under the account limit when returned. |
| `gpu_limit` | number | Provider GPU limit field when returned. |
| `limit` | number | Configured GPU limit. |
| `used` | number | Current GPU usage when returned. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /v1/me/gpu_limit` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-gpu-limit.md) for the provider-specific parameters and requirements.

