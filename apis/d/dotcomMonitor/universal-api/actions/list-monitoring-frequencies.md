# Dotcom Monitor: List Monitoring Frequencies

Retrieves monitoring frequencies for a platform from Dotcom Monitor.

```
GET https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/list-monitoring-frequencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotcom Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/list-monitoring-frequencies?connectionId=$CONNECTION_ID&platformName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "platformName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/list-monitoring-frequencies?${params}`, {
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

Through the native Dotcom Monitor API, this operation is `GET /frequencies/:platform_name` (base URL `https://api.dotcom-monitor.com/config_api_v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-monitoring-frequencies.md) for the provider-specific parameters and requirements.

