# PiAPI/Flux.1: Get Account Info

Retrieves your account information from PiAPI/Flux.1.

```
GET https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Flux.1 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/get-account-info?${params}`, {
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
      "code": 1,
      "data": {
        "equivalent_in_usd": 1,
        "id": 1,
        "is_enable": true,
        "max_concurrent_task_count": 1,
        "name": "Ava Chen",
        "plan": "string",
        "wallet": {
          "mj_remain": 1,
          "point_remain": 1
        }
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data.equivalent_in_usd` | number |  |
| `data.id` | number |  |
| `data.is_enable` | boolean |  |
| `data.max_concurrent_task_count` | number |  |
| `data.name` | string |  |
| `data.plan` | string |  |
| `data.wallet.mj_remain` | number |  |
| `data.wallet.point_remain` | number |  |
| `message` | string |  |

## Native endpoint

Through the native PiAPI/Flux.1 API, this operation is `GET /account/info` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

