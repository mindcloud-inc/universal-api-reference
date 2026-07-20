# New Relic Universal API Examples

These examples use the MindCloud API key and New Relic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Applications

Retrieves applications from New Relic.

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

Example response:

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

See the full [List Applications action reference](actions/list-applications.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/newRelic/latest/actions/list-applications).

## Add Entity To Alert Condition

Adds an entity to an alert condition in New Relic.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/add-entity-to-alert-condition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conditionId": 1,
  "entityId": 1,
  "entityType": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/add-entity-to-alert-condition', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conditionId": 1,
    "entityId": 1,
    "entityType": "0"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "condition": {
        "condition_scope": "string",
        "enabled": true,
        "entities": [
          1
        ],
        "id": 1,
        "metric": "string",
        "name": "Ava Chen",
        "runbook_url": "https://example.com",
        "terms": [
          {
            "duration": "string",
            "operator": "string",
            "priority": "string",
            "threshold": "string",
            "time_function": "string"
          }
        ],
        "type": "string",
        "violation_close_timer": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Entity To Alert Condition action reference](actions/add-entity-to-alert-condition.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/newRelic/latest/actions/add-entity-to-alert-condition).
