# Voog: List Webhooks

Retrieves webhooks for the current Voog site.

```
GET https://connect.mindcloud.co/v1/universal/voog/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voog `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voog/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voog/latest/actions/list-webhooks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voog API returns.

## Native endpoint

Through the native Voog API, this operation is `GET /webhooks` (base URL `{{credentials.siteUrl}}/admin/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

