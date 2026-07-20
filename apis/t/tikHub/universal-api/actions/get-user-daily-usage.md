# TikHub: Get User Daily Usage

Retrieves daily API usage from TikHub.

```
GET https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-user-daily-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-user-daily-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-user-daily-usage?${params}`, {
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
      "code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |

## Native endpoint

Through the native TikHub API, this operation is `GET /api/v1/tikhub/user/get_user_daily_usage` (base URL `https://api.tikhub.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-daily-usage.md) for the provider-specific parameters and requirements.

