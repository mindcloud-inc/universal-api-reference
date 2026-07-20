# Hoversignal: List Signal Leads



```
GET https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/list-signal-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hoversignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/list-signal-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/list-signal-leads?${params}`, {
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
          "discount": 1,
          "email": "ava@example.com",
          "id": 1,
          "phone": "string",
          "signalId": 1,
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
| `leads` | array<object> | The list of leads captured by Hoversignal signals. |
| `leads[].discount` | number | The captured discount amount when available. |
| `leads[].email` | string | The captured lead email address when available. |
| `leads[].id` | number | The lead identifier. |
| `leads[].phone` | string | The captured lead phone number when available. |
| `leads[].signalId` | number | The identifier of the signal that captured the lead. |
| `leads[].url` | string | The page URL where the lead was captured. |

## Native endpoint

Through the native Hoversignal API, this operation is `GET /api/v1/leads` (base URL `https://app.hoversignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signal-leads.md) for the provider-specific parameters and requirements.

