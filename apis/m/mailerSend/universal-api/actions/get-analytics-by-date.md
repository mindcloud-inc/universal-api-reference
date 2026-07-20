# MailerSend: Get Analytics By Date



```
GET https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-analytics-by-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-analytics-by-date?connectionId=$CONNECTION_ID&dateFrom=string&dateTo=string&event=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateFrom": "string",
  "dateTo": "string",
  "event": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-analytics-by-date?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateFrom` | string | yes | Start datetime for analytics results in YYYY-MM-DD HH:mm:ss format. |
| `dateTo` | string | yes | End datetime for analytics results in YYYY-MM-DD HH:mm:ss format. |
| `event` | string | yes | Analytics event types to include. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateFrom": "string",
      "dateTo": "string",
      "groupBy": "string",
      "stats": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateFrom` | string | Analytics date range start returned by MailerSend. |
| `dateTo` | string | Analytics date range end returned by MailerSend. |
| `groupBy` | string | Aggregation grouping used for the analytics response. |
| `stats` | array<object> | Per-period analytics stats rows returned by MailerSend. |

## Native endpoint

Through the native MailerSend API, this operation is `GET /analytics/date` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-analytics-by-date.md) for the provider-specific parameters and requirements.

