# Instructure: Hide All Stream Items

Hides all stream items in Instructure Canvas.

```
DELETE https://connect.mindcloud.co/v1/universal/instructure/latest/actions/hide-all-stream-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/hide-all-stream-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/hide-all-stream-items?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "hidden": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hidden` | boolean |  |

## Native endpoint

Through the native Instructure API, this operation is `DELETE /users/self/activity_stream` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/hide-all-stream-items.md) for the provider-specific parameters and requirements.

