# Rachio Smart Hose Timer: List Device Events

Retrieves device event records from Rachio.

```
GET https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/list-device-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Hose Timer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/list-device-events?connectionId=$CONNECTION_ID&endTime=1&id=string&startTime=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endTime": "1",
  "id": "string",
  "startTime": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/list-device-events?${params}`, {
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
| `endTime` | number | yes | Query end time in Unix epoch milliseconds. |
| `id` | string | yes | Controller device UUID. |
| `startTime` | number | yes | Query start time in Unix epoch milliseconds. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rachio Smart Hose Timer API returns.

## Native endpoint

Through the native Rachio Smart Hose Timer API, this operation is `GET /public/device/:id/event` (base URL `https://api.rach.io/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-device-events.md) for the provider-specific parameters and requirements.

