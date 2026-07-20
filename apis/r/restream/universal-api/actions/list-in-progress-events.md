# Restream: List In Progress Events

Retrieves in-progress events from Restream.

```
GET https://connect.mindcloud.co/v1/universal/restream/latest/actions/list-in-progress-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restream/latest/actions/list-in-progress-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restream/latest/actions/list-in-progress-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restream API returns.

## Native endpoint

Through the native Restream API, this operation is `GET /user/events/in-progress` (base URL `https://api.restream.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-in-progress-events.md) for the provider-specific parameters and requirements.

