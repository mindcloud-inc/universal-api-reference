# SIGNL4: Delete Event Source

Deletes an event source from SIGNL4.

```
DELETE https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/delete-event-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/delete-event-source?connectionId=$CONNECTION_ID&eventSourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventSourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/delete-event-source?${params}`, {
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
| `eventSourceId` | string | yes | ID of event source |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SIGNL4 API returns.

## Native endpoint

Through the native SIGNL4 API, this operation is `DELETE /v2/eventsources/{eventSourceId}` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-event-source.md) for the provider-specific parameters and requirements.

