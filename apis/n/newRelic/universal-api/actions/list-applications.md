# New Relic: List Applications

Retrieves applications from New Relic.

```
GET https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-applications?${params}`, {
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
      "applications": [
        {
          "application_summary": {
            "apdex_score": 1,
            "apdex_target": 1,
            "error_rate": 1,
            "response_time": 1,
            "throughput": 1
          },
          "end_user_summary": {
            "apdex_score": 1,
            "apdex_target": 1,
            "response_time": 1,
            "throughput": 1
          },
          "health_status": "string",
          "id": 1,
          "language": "string",
          "last_reported_at": "2026-05-07T12:00:00.000Z",
          "links": {
            "alert_policy": 1,
            "application_hosts": [
              1
            ],
            "application_instances": [
              1
            ]
          },
          "name": "Ava Chen",
          "reporting": true,
          "settings": {
            "app_apdex_threshold": 1,
            "enable_real_user_monitoring": true,
            "end_user_apdex_threshold": 1,
            "use_server_side_config": true
          }
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
| `applications[].application_summary.apdex_score` | number |  |
| `applications[].application_summary.apdex_target` | number |  |
| `applications[].application_summary.error_rate` | number |  |
| `applications[].application_summary.response_time` | number |  |
| `applications[].application_summary.throughput` | number |  |
| `applications[].end_user_summary.apdex_score` | number |  |
| `applications[].end_user_summary.apdex_target` | number |  |
| `applications[].end_user_summary.response_time` | number |  |
| `applications[].end_user_summary.throughput` | number |  |
| `applications[].health_status` | string |  |
| `applications[].id` | number |  |
| `applications[].language` | string |  |
| `applications[].last_reported_at` | date |  |
| `applications[].links.alert_policy` | number |  |
| `applications[].links.application_hosts[]` | number |  |
| `applications[].links.application_instances[]` | number |  |
| `applications[].name` | string |  |
| `applications[].reporting` | boolean |  |
| `applications[].settings.app_apdex_threshold` | number |  |
| `applications[].settings.enable_real_user_monitoring` | boolean |  |
| `applications[].settings.end_user_apdex_threshold` | number |  |
| `applications[].settings.use_server_side_config` | boolean |  |

## Native endpoint

Through the native New Relic API, this operation is `GET /applications.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-applications.md) for the provider-specific parameters and requirements.

