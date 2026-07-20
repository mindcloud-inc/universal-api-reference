# Brevo: Get SMTP Aggregated Report



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-smtp-aggregated-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-smtp-aggregated-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-smtp-aggregated-report?${params}`, {
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
      "blocked": 1,
      "clicks": 1,
      "delivered": 1,
      "hardBounces": 1,
      "invalid": 1,
      "opens": 1,
      "range": "string",
      "requests": 1,
      "softBounces": 1,
      "spamReports": 1,
      "unsubscribed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | number | The blocked count. |
| `clicks` | number | The click count. |
| `delivered` | number | The delivered count. |
| `hardBounces` | number | The hard bounce count. |
| `invalid` | number | The invalid count. |
| `opens` | number | The open count. |
| `range` | string | The covered date range. |
| `requests` | number | The request count. |
| `softBounces` | number | The soft bounce count. |
| `spamReports` | number | The spam report count. |
| `unsubscribed` | number | The unsubscribed count. |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/smtp/statistics/aggregatedReport` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-smtp-aggregated-report.md) for the provider-specific parameters and requirements.

