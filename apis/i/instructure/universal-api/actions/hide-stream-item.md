# Instructure: Hide Stream Item

Hides a stream item in Instructure Canvas.

```
DELETE https://connect.mindcloud.co/v1/universal/instructure/latest/actions/hide-stream-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/hide-stream-item?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/hide-stream-item?${params}`, {
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
| `id` | string | yes | ID of the activity stream item to hide. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html_url": "https://example.com",
      "id": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html_url` | string |  |
| `id` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `DELETE /users/self/activity_stream/:id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/hide-stream-item.md) for the provider-specific parameters and requirements.

