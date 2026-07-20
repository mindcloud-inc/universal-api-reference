# Datadog: Delete Monitor

Deletes an existing monitor from Datadog.

```
DELETE https://connect.mindcloud.co/v1/universal/datadog/latest/actions/delete-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/delete-monitor?connectionId=$CONNECTION_ID&monitorId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "monitorId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/delete-monitor?${params}`, {
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
| `monitorId` | number | yes | The ID of the monitor to delete. |
| `force` | string | no | Delete the monitor even if it is referenced by other resources. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedMonitorId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedMonitorId` | number | ID of the deleted monitor. |

## Native endpoint

Through the native Datadog API, this operation is `DELETE /api/v1/monitor/:monitor_id` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-monitor.md) for the provider-specific parameters and requirements.

