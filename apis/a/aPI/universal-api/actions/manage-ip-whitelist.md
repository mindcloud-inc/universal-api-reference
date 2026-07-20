# 44API: Manage IP Whitelist

Manages the IP whitelist in 44API by adding, removing, or listing IPs.

```
PUT https://connect.mindcloud.co/v1/universal/aPI/latest/actions/manage-ip-whitelist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 44API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aPI/latest/actions/manage-ip-whitelist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aPI/latest/actions/manage-ip-whitelist', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Use add, remove, or list. |
| `ipAddress` | string | no | IP address required for add and remove actions. |
| `email` | string | no | Verification email required for add. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 44API API returns.

## Native endpoint

Through the native 44API API, this operation is `POST /webhook/ip-whitelist` (base URL `https://api.44api.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/manage-ip-whitelist.md) for the provider-specific parameters and requirements.

