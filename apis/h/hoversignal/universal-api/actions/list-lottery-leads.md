# Hoversignal: List Lottery Leads



```
GET https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/list-lottery-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hoversignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/list-lottery-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/list-lottery-leads?${params}`, {
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
      "leads": [
        {
          "email": "ava@example.com",
          "id": 1,
          "lotteryId": 1,
          "phone": "string",
          "url": "https://example.com"
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
| `leads` | array<object> | The list of lottery leads captured by Hoversignal. |
| `leads[].email` | string | The captured lottery lead email address when available. |
| `leads[].id` | number | The lottery lead identifier. |
| `leads[].lotteryId` | number | The lottery identifier associated with the lead. |
| `leads[].phone` | string | The captured lottery lead phone number when available. |
| `leads[].url` | string | The page URL where the lottery lead was captured. |

## Native endpoint

Through the native Hoversignal API, this operation is `GET /api/v1/leads/lottery` (base URL `https://app.hoversignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lottery-leads.md) for the provider-specific parameters and requirements.

