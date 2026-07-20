# Frappe: Call Whitelisted Method V1 (POST)

Calls a whitelisted Frappe method with POST.

```
POST https://connect.mindcloud.co/v1/universal/frappe/latest/actions/call-whitelisted-method-v1-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frappe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frappe/latest/actions/call-whitelisted-method-v1-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frappe/latest/actions/call-whitelisted-method-v1-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Frappe API returns.

## Native endpoint

Through the native Frappe API, this operation is `POST /api/method/{{arguments.methodPath}}` (base URL `{{credentials.siteUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/call-whitelisted-method-v1-post.md) for the provider-specific parameters and requirements.

