# PiAPI/Skyreels: Get Account Info

Retrieves information about your PiAPI account.

```
GET https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Skyreels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/get-account-info?${params}`, {
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
        "account_group": "string",
        "id": 1,
        "is_enable": true,
        "is_verified": true,
        "max_concurrent_task_count": 1,
        "name": "Ava Chen",
        "plan": "string",
        "platform": "string",
        "type": "string",
        "wallet": {
          "id": 1,
          "point_frozen": 1,
          "point_remain": 1,
          "point_used": 1
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
| `data.account_group` | string |  |
| `data.id` | number |  |
| `data.is_enable` | boolean |  |
| `data.is_verified` | boolean |  |
| `data.max_concurrent_task_count` | number |  |
| `data.name` | string |  |
| `data.plan` | string |  |
| `data.platform` | string |  |
| `data.type` | string |  |
| `data.wallet.id` | number |  |
| `data.wallet.point_frozen` | number |  |
| `data.wallet.point_remain` | number |  |
| `data.wallet.point_used` | number |  |
| `message` | string |  |

## Native endpoint

Through the native PiAPI/Skyreels API, this operation is `GET /account/info` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

