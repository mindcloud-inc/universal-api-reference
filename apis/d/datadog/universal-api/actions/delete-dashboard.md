# Datadog: Delete Dashboard

Deletes an existing dashboard from Datadog.

```
DELETE https://connect.mindcloud.co/v1/universal/datadog/latest/actions/delete-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/delete-dashboard?connectionId=$CONNECTION_ID&dashboardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dashboardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/delete-dashboard?${params}`, {
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
| `dashboardId` | string | yes | The ID of the dashboard. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Datadog API returns.

## Native endpoint

Through the native Datadog API, this operation is `DELETE /api/v1/dashboard/:dashboard_id` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-dashboard.md) for the provider-specific parameters and requirements.

