# AskHandle: List Keyword Notifications

Retrieves keyword notifications from your AskHandle account.

```
GET https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/list-keyword-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AskHandle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/list-keyword-notifications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/list-keyword-notifications?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AskHandle API returns.

## Native endpoint

Through the native AskHandle API, this operation is `GET /keyword_notifications/` (base URL `https://dashboard.askhandle.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-keyword-notifications.md) for the provider-specific parameters and requirements.

