# Galileo: List Project Alerts

Finds alerts for a Galileo project.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-project-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-project-alerts?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-project-alerts?${params}`, {
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
| `projectId` | string | yes | Galileo project UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alerts": [
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
      "limit": 1,
      "nextStartingToken": 1,
      "paginated": true,
      "startingToken": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alerts` | array<object> |  |
| `alerts[].active` | boolean |  |
| `alerts[].conditions` | array<object> |  |
| `alerts[].conditions[].aggregation` | string |  |
| `alerts[].conditions[].conditionType` | string |  |
| `alerts[].conditions[].field` | string |  |
| `alerts[].conditions[].filterOperator` | string |  |
| `alerts[].conditions[].filterValue` | string |  |
| `alerts[].conditions[].operator` | string |  |
| `alerts[].conditions[].value` | number |  |
| `alerts[].conditions[].window` | number |  |
| `alerts[].createdAt` | date |  |
| `alerts[].createdBy` | string |  |
| `alerts[].filters` | array<object> |  |
| `alerts[].filters[].caseSensitive` | boolean |  |
| `alerts[].filters[].name` | string |  |
| `alerts[].filters[].operator` | string |  |
| `alerts[].filters[].value` | string |  |
| `alerts[].id` | string |  |
| `alerts[].interval` | number |  |
| `alerts[].projectId` | string |  |
| `alerts[].schemaVersion` | string |  |
| `alerts[].updatedAt` | date |  |
| `limit` | number |  |
| `nextStartingToken` | number |  |
| `paginated` | boolean |  |
| `startingToken` | number |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/projects/:project_id/alerts` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-alerts.md) for the provider-specific parameters and requirements.

