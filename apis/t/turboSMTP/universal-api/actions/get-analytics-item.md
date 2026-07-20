# turboSMTP: Get Analytics Item

Retrieves an analytics item from turboSMTP.

```
GET https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-analytics-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-analytics-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-analytics-item?${params}`, {
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
      "domain": "string",
      "error": "string",
      "id": 1,
      "recipient": "string",
      "recipient_domain": "string",
      "send_time": "string",
      "sender": "string",
      "status": "string",
      "subject": "string",
      "x_campaign_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `error` | string |  |
| `id` | number |  |
| `recipient` | string |  |
| `recipient_domain` | string |  |
| `send_time` | string |  |
| `sender` | string |  |
| `status` | string |  |
| `subject` | string |  |
| `x_campaign_id` | string |  |

## Native endpoint

Through the native turboSMTP API, this operation is `GET /analytics/{Id}` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-analytics-item.md) for the provider-specific parameters and requirements.

