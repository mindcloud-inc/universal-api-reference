# IronWiFi: Get Accounting Report

Retrieves RADIUS accounting logs from IronWiFi.

```
GET https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/get-accounting-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IronWiFi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/get-accounting-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/get-accounting-report?${params}`, {
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
      "graph": {},
      "id": "string",
      "links": {},
      "scheduledReports": [
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
| `graph` | object | Graph configuration and dataset metadata for the accounting report. |
| `id` | string | IronWiFi report identifier. |
| `links` | object | HAL link metadata returned by IronWiFi. |
| `scheduledReports` | array<object> | Scheduled report runs configured for this report. |

## Native endpoint

Through the native IronWiFi API, this operation is `GET /reports/111` (base URL `https://console.ironwifi.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-accounting-report.md) for the provider-specific parameters and requirements.

