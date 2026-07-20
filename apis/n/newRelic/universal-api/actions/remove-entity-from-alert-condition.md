# New Relic: Remove Entity From Alert Condition

Removes an entity from an alert condition in New Relic.

```
DELETE https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/remove-entity-from-alert-condition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/remove-entity-from-alert-condition?connectionId=$CONNECTION_ID&conditionId=1&entityId=1&entityType=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conditionId": "1",
  "entityId": "1",
  "entityType": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/remove-entity-from-alert-condition?${params}`, {
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
| `conditionId` | number | yes | Alert condition ID that currently includes the entity. |
| `entityId` | number | yes | New Relic alert entity ID. |
| `entityType` | list | yes | Entity type: Application, BrowserApplication, MobileApplication, or KeyTransaction. One of: `0`, `1`, `2`, `3`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `condition.condition_scope` | string |  |
| `condition.enabled` | boolean |  |
| `condition.entities[]` | number |  |
| `condition.id` | number |  |
| `condition.metric` | string |  |
| `condition.name` | string |  |
| `condition.runbook_url` | string |  |
| `condition.terms[].duration` | string |  |
| `condition.terms[].operator` | string |  |
| `condition.terms[].priority` | string |  |
| `condition.terms[].threshold` | string |  |
| `condition.terms[].time_function` | string |  |
| `condition.type` | string |  |
| `condition.violation_close_timer` | number |  |

## Native endpoint

Through the native New Relic API, this operation is `DELETE /alerts_entity_conditions/:entityId.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-entity-from-alert-condition.md) for the provider-specific parameters and requirements.

