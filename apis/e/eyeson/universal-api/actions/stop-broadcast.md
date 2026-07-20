# Eyeson: Stop Broadcast



```
DELETE https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/stop-broadcast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eyeson `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/stop-broadcast?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/stop-broadcast?${params}`, {
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
| `accessKey` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eyeson API returns.

## Native endpoint

Through the native Eyeson API, this operation is `DELETE /rooms/:accessKey/broadcasts` (base URL `https://api.eyeson.team`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-broadcast.md) for the provider-specific parameters and requirements.

