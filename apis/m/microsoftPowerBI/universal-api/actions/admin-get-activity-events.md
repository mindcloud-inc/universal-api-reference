# Microsoft Power BI: Get Activity Events



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-get-activity-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-get-activity-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-get-activity-events?${params}`, {
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
| `_filter` | string | no | Filters the results based on a boolean condition, using 'Activity', 'UserId', or both properties. Supports only 'eq' and 'and' operators. |
| `continuationToken` | string | no | Token required to get the next chunk of the result set |
| `endDateTime` | string | no | End date and time of the window for audit event results. Must be in ISO 8601 compliant UTC format. |
| `startDateTime` | string | no | Start date and time of the window for audit event results. Must be in ISO 8601 compliant UTC format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET admin/activityevents` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/admin-get-activity-events.md) for the provider-specific parameters and requirements.

