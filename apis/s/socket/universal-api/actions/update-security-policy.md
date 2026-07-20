# Socket: Update Security Policy

Updates an organization security policy in Socket.

```
PUT https://connect.mindcloud.co/v1/universal/socket/latest/actions/update-security-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/socket/latest/actions/update-security-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/update-security-policy', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Socket API returns.

## Native endpoint

Through the native Socket API, this operation is `POST /orgs/:org_slug/settings/security-policy` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-security-policy.md) for the provider-specific parameters and requirements.

