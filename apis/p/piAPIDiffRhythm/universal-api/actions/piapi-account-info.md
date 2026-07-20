# PiAPI/DiffRhythm: PiAPI Account Info

Retrieves your account information from PiAPI/DiffRhythm.

```
GET https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/piapi-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/DiffRhythm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/piapi-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/piapi-account-info?${params}`, {
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
      "credit_pack_info": {
        "available_credits": 1
      },
      "equivalent_in_usd": 1,
      "id": 1,
      "max_concurrent_task_count": 1,
      "name": "Ava Chen",
      "plan": "string",
      "type": "string",
      "wallet": {
        "llm_remain": 1,
        "llm_used": 1,
        "point_remain": 1,
        "point_used": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credit_pack_info.available_credits` | number |  |
| `equivalent_in_usd` | number |  |
| `id` | number |  |
| `max_concurrent_task_count` | number |  |
| `name` | string |  |
| `plan` | string |  |
| `type` | string |  |
| `wallet.llm_remain` | number |  |
| `wallet.llm_used` | number |  |
| `wallet.point_remain` | number |  |
| `wallet.point_used` | number |  |

## Native endpoint

Through the native PiAPI/DiffRhythm API, this operation is `GET /account/info` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/piapi-account-info.md) for the provider-specific parameters and requirements.

