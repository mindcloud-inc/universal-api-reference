# IronWiFi: Get Authentication Report

Retrieves RADIUS authentication logs from IronWiFi.

```
GET https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/get-authentication-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IronWiFi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/get-authentication-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/get-authentication-report?${params}`, {
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
      "id": "string",
      "links": {},
      "scheduledReports": [
        {}
      ],
      "taskName": "Ava Chen",
      "visibleColumns": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | IronWiFi report identifier. |
| `links` | object | HAL link metadata returned by IronWiFi. |
| `scheduledReports` | array<object> | Scheduled report runs configured for this report. |
| `taskName` | string | Name of the IronWiFi authentication report task. |
| `visibleColumns` | array<string> | Columns configured to appear in the report. |

## Native endpoint

Through the native IronWiFi API, this operation is `GET /reports/110` (base URL `https://console.ironwifi.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authentication-report.md) for the provider-specific parameters and requirements.

