# Livestorm: Remove Event Tag

Removes a tag from an event in Livestorm.

```
DELETE https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/remove-event-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/remove-event-tag?connectionId=$CONNECTION_ID&id=string&data.attributes.title=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "data.attributes.title": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/remove-event-tag?${params}`, {
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
| `data.attributes.title` | string | yes | Tag title to remove |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Livestorm API returns.

## Native endpoint

Through the native Livestorm API, this operation is `DELETE events/:id/tags` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-event-tag.md) for the provider-specific parameters and requirements.

