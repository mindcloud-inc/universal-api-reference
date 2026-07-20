# Galileo: Get Project Alert

Retrieves an alert from a Galileo project by ID.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-project-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-project-alert?connectionId=$CONNECTION_ID&monitorAlertConfigId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "monitorAlertConfigId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-project-alert?${params}`, {
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
| `monitorAlertConfigId` | string | yes | Galileo monitor alert configuration UUID. |
| `projectId` | string | yes | Galileo project UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "conditions": [
        {
          "aggregation": "string",
          "conditionType": "string",
          "field": "string",
          "filterOperator": "string",
          "filterValue": "string",
          "operator": "string",
          "value": 1,
          "window": 1
        }
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "filters": [
        {
          "caseSensitive": true,
          "name": "Ava Chen",
          "operator": "string",
          "value": "string"
        }
      ],
      "id": "string",
      "interval": 1,
      "projectId": "string",
      "schemaVersion": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `conditions` | array<object> |  |
| `conditions[].aggregation` | string |  |
| `conditions[].conditionType` | string |  |
| `conditions[].field` | string |  |
| `conditions[].filterOperator` | string |  |
| `conditions[].filterValue` | string |  |
| `conditions[].operator` | string |  |
| `conditions[].value` | number |  |
| `conditions[].window` | number |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `filters` | array<object> |  |
| `filters[].caseSensitive` | boolean |  |
| `filters[].name` | string |  |
| `filters[].operator` | string |  |
| `filters[].value` | string |  |
| `id` | string |  |
| `interval` | number |  |
| `projectId` | string |  |
| `schemaVersion` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/projects/:project_id/alerts/:monitor_alert_config_id` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-alert.md) for the provider-specific parameters and requirements.

