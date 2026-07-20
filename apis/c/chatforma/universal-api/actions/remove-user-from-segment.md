# Chatforma: Remove User From Segment

Deletes a user from a Chatforma segment.

```
DELETE https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/remove-user-from-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatforma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/remove-user-from-segment?connectionId=$CONNECTION_ID&botId=1&segmentId=1&botUserId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "1",
  "segmentId": "1",
  "botUserId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/remove-user-from-segment?${params}`, {
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
| `botId` | number | yes |  |
| `segmentId` | number | yes |  |
| `botUserId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chatforma API returns.

## Native endpoint

Through the native Chatforma API, this operation is `DELETE /bots/:botId/segments/:segmentId/users` (base URL `https://api.pro.chatforma.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user-from-segment.md) for the provider-specific parameters and requirements.

