# Livestorm: Delete Event

Deletes an existing event from Livestorm.

```
DELETE https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/delete-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/delete-event?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/delete-event?${params}`, {
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
| `id` | string | yes | Event ID |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Livestorm API returns.

## Native endpoint

Through the native Livestorm API, this operation is `DELETE events/:id` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-event.md) for the provider-specific parameters and requirements.

