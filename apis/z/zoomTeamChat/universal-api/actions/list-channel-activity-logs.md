# Zoom Team Chat: List Channel Activity Logs



```
GET https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-channel-activity-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-channel-activity-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&channelId=string&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "channelId": "string",
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-channel-activity-logs?${params}`, {
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
| `channelId` | string | yes | The channel's unique identifier. |
| `activityType` | string | no | The activity log type. |
| `startDate` | string | yes | The activity log start date in YYYY-MM-DD format. |
| `endDate` | string | yes | The activity log end date in YYYY-MM-DD format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoom Team Chat API returns.

## Native endpoint

Through the native Zoom Team Chat API, this operation is `GET /chat/channels/:channelId/activities` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-channel-activity-logs.md) for the provider-specific parameters and requirements.

