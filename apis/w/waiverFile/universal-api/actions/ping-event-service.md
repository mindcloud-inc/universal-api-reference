# WaiverFile: Ping Event Service

Checks whether WaiverFile's event service is live.

```
GET https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/ping-event-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/ping-event-service?connectionId=$CONNECTION_ID&val=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "val": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/ping-event-service?${params}`, {
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
| `val` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WaiverFile API returns.

## Native endpoint

Through the native WaiverFile API, this operation is `POST /EvtPing` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ping-event-service.md) for the provider-specific parameters and requirements.

