# Subpage: List New Articles



```
GET https://connect.mindcloud.co/v1/universal/subpage/latest/actions/list-new-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Subpage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/subpage/latest/actions/list-new-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/subpage/latest/actions/list-new-articles?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Subpage API returns.

## Native endpoint

Through the native Subpage API, this operation is `GET /call/api/zapier/listtrigger` (base URL `https://editor.subpage.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-new-articles.md) for the provider-specific parameters and requirements.

