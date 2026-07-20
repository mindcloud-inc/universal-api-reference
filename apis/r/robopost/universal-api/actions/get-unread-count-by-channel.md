# Robopost: Get Unread Count by Channel

Retrieves unread inbox counts by channel from Robopost.

```
GET https://connect.mindcloud.co/v1/universal/robopost/latest/actions/get-unread-count-by-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Robopost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/robopost/latest/actions/get-unread-count-by-channel?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/robopost/latest/actions/get-unread-count-by-channel?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Robopost API returns.

## Native endpoint

Through the native Robopost API, this operation is `GET /social_inbox_items/unread/by_channel` (base URL `https://public-api.robopost.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-unread-count-by-channel.md) for the provider-specific parameters and requirements.

