# Ahrefs: Get Metrics History



```
GET https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-metrics-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ahrefs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-metrics-history?connectionId=$CONNECTION_ID&target=string&dateFrom=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "string",
  "dateFrom": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-metrics-history?${params}`, {
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
| `target` | string | yes | Domain or URL to analyze. |
| `dateFrom` | date | yes | Start date in YYYY-MM-DD format. |
| `dateTo` | date | no | End date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "orgTraffic": 1,
      "orgCost": 1,
      "paidTraffic": 1,
      "paidCost": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | History period date. |
| `orgTraffic` | number | Estimated monthly organic search traffic. |
| `orgCost` | number | Estimated monthly organic traffic value in USD cents. |
| `paidTraffic` | number | Estimated monthly paid search traffic. |
| `paidCost` | number | Estimated monthly paid traffic cost in USD cents. |

## Native endpoint

Through the native Ahrefs API, this operation is `GET /site-explorer/metrics-history` (base URL `https://api.ahrefs.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-metrics-history.md) for the provider-specific parameters and requirements.

