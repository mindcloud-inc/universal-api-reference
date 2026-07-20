# Selzy: Get Campaign Common Stats

Retrieves common campaign stats from Selzy.

```
GET https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-campaign-common-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-campaign-common-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-campaign-common-stats?${params}`, {
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
      "result": {
        "clicked_all": 1,
        "clicked_unique": 1,
        "delivered": 1,
        "read_all": 1,
        "read_unique": 1,
        "sent": 1,
        "spam": 1,
        "total": 1,
        "unsubscribed": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.clicked_all` | number |  |
| `result.clicked_unique` | number |  |
| `result.delivered` | number |  |
| `result.read_all` | number |  |
| `result.read_unique` | number |  |
| `result.sent` | number |  |
| `result.spam` | number |  |
| `result.total` | number |  |
| `result.unsubscribed` | number |  |

## Native endpoint

Through the native Selzy API, this operation is `POST getCampaignCommonStats` (base URL `https://api.selzy.com/en/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-common-stats.md) for the provider-specific parameters and requirements.

