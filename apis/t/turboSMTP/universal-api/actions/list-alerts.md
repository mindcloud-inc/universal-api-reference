# turboSMTP: List Alerts

Retrieves alerts from your turboSMTP account.

```
GET https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-alerts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-alerts?${params}`, {
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
      "count": 1,
      "results": [
        {
          "email": "ava@example.com",
          "id": 1,
          "percentage": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Total alert count. |
| `results[].email` | string | Alert email address. |
| `results[].id` | number | Alert ID. |
| `results[].percentage` | number | Alert percentage. |

## Native endpoint

Through the native turboSMTP API, this operation is `GET /tools/alerts` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alerts.md) for the provider-specific parameters and requirements.

