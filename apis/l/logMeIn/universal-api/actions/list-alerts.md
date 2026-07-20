# LogMeIn: List Alerts

Retrieves a filtered list of alerts from LogMeIn.

```
GET https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/list-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/list-alerts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/list-alerts?${params}`, {
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
| `pagination.pageSize` | number | no | Maximum number of alerts to return. GoTo caps a request at 200 alerts. |
| `filter.isAcknowledged` | boolean | no | When provided, returns either active or acknowledged alerts. |
| `filter.deviceIds[]` | array<string> | no | Device IDs to filter alerts by. |
| `filter.ruleTypes[]` | array<string> | no | Rule types to filter alerts by. |
| `filter.tenantIds[]` | array<string> | no | Tenant IDs to filter alerts by. |
| `filter.priorities[]` | array<string> | no | Alert priorities to filter by. |
| `filter.triggeredBefore` | date | no | Return alerts triggered before this timestamp. |
| `filter.triggeredAfter` | date | no | Return alerts triggered after this timestamp. |
| `sorting.property` | string | no | Alert property to sort by. |
| `sorting.order` | string | no | Sort order for alerts. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pagination.continuationToken` | string | no | Continuation token for the next page of alerts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alertId": "string",
      "deviceId": "string",
      "priority": "string",
      "status": "string",
      "triggeredAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alertId` | string |  |
| `deviceId` | string |  |
| `priority` | string |  |
| `status` | string |  |
| `triggeredAt` | date |  |

## Native endpoint

Through the native LogMeIn API, this operation is `POST /goto-resolve-alerts/v1/alerts/list` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alerts.md) for the provider-specific parameters and requirements.

