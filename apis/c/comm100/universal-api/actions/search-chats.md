# Comm100: Search Chats

Searches live chat conversations in Comm100.

```
GET https://connect.mindcloud.co/v1/universal/comm100/latest/actions/search-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Comm100 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comm100/latest/actions/search-chats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comm100/latest/actions/search-chats?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Comm100 API returns.

## Native endpoint

Through the native Comm100 API, this operation is `POST livechat/chats\:Search` (base URL `https://api17.comm100.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-chats.md) for the provider-specific parameters and requirements.

