# EARLY: Cancel Tracking

Cancels the current tracking session in EARLY.

```
DELETE https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/cancel-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EARLY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/cancel-tracking?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/cancel-tracking?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EARLY API returns.

## Native endpoint

Through the native EARLY API, this operation is `DELETE /api/v4/tracking` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-tracking.md) for the provider-specific parameters and requirements.

