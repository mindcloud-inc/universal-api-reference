# Dotcom Monitor: List Monitoring Locations

Retrieves monitoring locations for a platform from Dotcom Monitor.

```
GET https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/list-monitoring-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotcom Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/list-monitoring-locations?connectionId=$CONNECTION_ID&platformName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "platformName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/list-monitoring-locations?${params}`, {
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
| `platformName` | string | yes | Platform name segment from Dotcom Monitor monitoring platforms. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dotcom Monitor API returns.

## Native endpoint

Through the native Dotcom Monitor API, this operation is `GET /locations/:platform_name` (base URL `https://api.dotcom-monitor.com/config_api_v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-monitoring-locations.md) for the provider-specific parameters and requirements.

