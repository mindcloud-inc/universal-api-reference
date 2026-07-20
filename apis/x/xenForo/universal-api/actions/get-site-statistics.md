# XenForo: Get Site Statistics

Retrieves public site statistics from XenForo.

```
GET https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-site-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-site-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-site-statistics?${params}`, {
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
      "latest_user[register_date]": 1,
      "latest_user[user_id]": 1,
      "latest_user[username]": "Ava Chen",
      "online[guests]": 1,
      "online[members]": 1,
      "online[total]": 1,
      "totals[messages]": 1,
      "totals[threads]": 1,
      "totals[users]": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `latest_user[register_date]` | number |  |
| `latest_user[user_id]` | number |  |
| `latest_user[username]` | string |  |
| `online[guests]` | number |  |
| `online[members]` | number |  |
| `online[total]` | number |  |
| `totals[messages]` | number |  |
| `totals[threads]` | number |  |
| `totals[users]` | number |  |

## Native endpoint

Through the native XenForo API, this operation is `GET /stats/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-statistics.md) for the provider-specific parameters and requirements.

