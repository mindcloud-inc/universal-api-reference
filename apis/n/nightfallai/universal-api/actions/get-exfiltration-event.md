# Nightfall.ai: Get Exfiltration Event

Retrieves an exfiltration event from Nightfall.ai.

```
GET https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/get-exfiltration-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nightfall.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/get-exfiltration-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/get-exfiltration-event?${params}`, {
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
| `eventId` | string | yes | The UUID of the exfiltration event to fetch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nightfall.ai API returns.

## Native endpoint

Through the native Nightfall.ai API, this operation is `GET /exfiltration/v1/events/:eventId` (base URL `https://api.nightfall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-exfiltration-event.md) for the provider-specific parameters and requirements.

