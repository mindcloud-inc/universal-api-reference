# Kit: Remove Tag From Subscriber

Removes a tag from a Kit subscriber.

```
DELETE https://connect.mindcloud.co/v1/universal/kit/latest/actions/remove-tag-from-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kit/latest/actions/remove-tag-from-subscriber?connectionId=$CONNECTION_ID&tagId=1&subscriberId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagId": "1",
  "subscriberId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kit/latest/actions/remove-tag-from-subscriber?${params}`, {
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
| `tagId` | number | yes | Tag ID from the path parameter. |
| `subscriberId` | number | yes | Subscriber ID from the path parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kit API returns.

## Native endpoint

Through the native Kit API, this operation is `DELETE /tags/:tag_id/subscribers/:id` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tag-from-subscriber.md) for the provider-specific parameters and requirements.

