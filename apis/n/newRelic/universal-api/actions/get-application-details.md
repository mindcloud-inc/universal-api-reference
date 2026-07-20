# New Relic: Get Application Details

Retrieves application details from New Relic.

```
GET https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/get-application-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/get-application-details?connectionId=$CONNECTION_ID&appId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/get-application-details?${params}`, {
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
| `appId` | number | yes | New Relic application ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "application": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application.application_summary.apdex_score` | number |  |
| `application.application_summary.apdex_target` | number |  |
| `application.application_summary.error_rate` | number |  |
| `application.application_summary.response_time` | number |  |
| `application.application_summary.throughput` | number |  |
| `application.end_user_summary.apdex_score` | number |  |
| `application.end_user_summary.apdex_target` | number |  |
| `application.end_user_summary.response_time` | number |  |
| `application.end_user_summary.throughput` | number |  |
| `application.health_status` | string |  |
| `application.id` | number |  |
| `application.language` | string |  |
| `application.last_reported_at` | date |  |
| `application.links.alert_policy` | number |  |
| `application.links.application_hosts[]` | number |  |
| `application.links.application_instances[]` | number |  |
| `application.name` | string |  |
| `application.reporting` | boolean |  |
| `application.settings.app_apdex_threshold` | number |  |
| `application.settings.enable_real_user_monitoring` | boolean |  |
| `application.settings.end_user_apdex_threshold` | number |  |
| `application.settings.use_server_side_config` | boolean |  |

## Native endpoint

Through the native New Relic API, this operation is `GET /applications/:appId.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-application-details.md) for the provider-specific parameters and requirements.

