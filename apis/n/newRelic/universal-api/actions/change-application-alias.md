# New Relic: Change Application Alias

Updates an application alias in New Relic.

```
PUT https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/change-application-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/change-application-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/change-application-alias', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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

Through the native New Relic API, this operation is `PUT /applications/:appId.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-application-alias.md) for the provider-specific parameters and requirements.

