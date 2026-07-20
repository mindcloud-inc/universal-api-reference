# Coralogix: List Alert Scheduler Rules



```
GET https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-alert-scheduler-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coralogix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-alert-scheduler-rules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-alert-scheduler-rules?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activeTimeframe` | string | no | Optional active_timeframe query parameter supported by the Coralogix OpenAPI endpoint. |
| `enabled` | boolean | no | Optional enabled query parameter supported by the Coralogix OpenAPI endpoint. |
| `alertSchedulerRulesIds` | string | no | Optional alert_scheduler_rules_ids query parameter supported by the Coralogix OpenAPI endpoint. |
| `nextPageToken` | string | no | Optional next_page_token query parameter supported by the Coralogix OpenAPI endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alertSchedulerRules": [
        {}
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alertSchedulerRules` | array<object> | alertSchedulerRules returned by Coralogix. |
| `nextPageToken` | string | nextPageToken returned by Coralogix. |

## Native endpoint

Through the native Coralogix API, this operation is `GET /v1/alert-scheduler-rules/bulk` (base URL `https://api.eu2.coralogix.com/mgmt/openapi/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alert-scheduler-rules.md) for the provider-specific parameters and requirements.

