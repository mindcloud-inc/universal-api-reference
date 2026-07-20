# Deep Infra: Get Deployment GPU Availability



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-deployment-gpu-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-deployment-gpu-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-deployment-gpu-availability?${params}`, {
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
      "gpu": "string",
      "memory": 1,
      "price": 1,
      "region": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | number | Number of available GPUs. |
| `gpu` | string | GPU type or SKU. |
| `memory` | number | GPU memory when returned. |
| `price` | number | GPU price when returned. |
| `region` | string | Availability region when returned. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /deploy/llm/gpu_availability` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment-gpu-availability.md) for the provider-specific parameters and requirements.

