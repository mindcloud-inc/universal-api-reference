# Delete Audit Log Event with SurveySparrow

Deletes a subscribed audit log event from SurveySparrow.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/audit_logs/events/{{id}}`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Delete Audit Log Event](https://developers.surveysparrow.com/rest-apis/delete-v-3-audit-logs-events-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Id of event to be deleted |
