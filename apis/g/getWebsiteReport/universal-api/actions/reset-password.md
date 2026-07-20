# Get Website Report: Reset Password



```
PUT https://connect.mindcloud.co/v1/universal/getWebsiteReport/latest/actions/reset-password
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Get Website Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/getWebsiteReport/latest/actions/reset-password" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getWebsiteReport/latest/actions/reset-password', {
  method: 'PUT',
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Get Website Report API returns.

## Native endpoint

Through the native Get Website Report API, this operation is `POST /users/reset-password` (base URL `https://gwr-v3-prod-dot-turing-alcove-395007.el.r.appspot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reset-password.md) for the provider-specific parameters and requirements.

