# Dotcom Monitor: Get Notification Group Info

Retrieves notification group details from Dotcom Monitor.

```
GET https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/get-notification-group-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotcom Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/get-notification-group-info?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/get-notification-group-info?${params}`, {
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
| `groupId` | string | yes | Unique notification group id from Get Notification Group List. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dotcom Monitor API returns.

## Native endpoint

Through the native Dotcom Monitor API, this operation is `GET /group/:group_id` (base URL `https://api.dotcom-monitor.com/config_api_v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification-group-info.md) for the provider-specific parameters and requirements.

