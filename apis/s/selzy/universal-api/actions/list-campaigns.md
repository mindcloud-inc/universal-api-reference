# Selzy: List Campaigns

Retrieves campaigns from Selzy.

```
GET https://connect.mindcloud.co/v1/universal/selzy/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selzy/latest/actions/list-campaigns?${params}`, {
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
      "result": [
        {
          "id": 1,
          "list_id": 1,
          "message_id": 1,
          "sender_email": "ava@example.com",
          "sender_name": "Ava Chen",
          "start_time": "string",
          "stats_url": "https://example.com",
          "status": "string",
          "subject": "string"
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
| `result[].id` | number |  |
| `result[].list_id` | number |  |
| `result[].message_id` | number |  |
| `result[].sender_email` | string |  |
| `result[].sender_name` | string |  |
| `result[].start_time` | string |  |
| `result[].stats_url` | string |  |
| `result[].status` | string |  |
| `result[].subject` | string |  |

## Native endpoint

Through the native Selzy API, this operation is `POST getCampaigns` (base URL `https://api.selzy.com/en/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

