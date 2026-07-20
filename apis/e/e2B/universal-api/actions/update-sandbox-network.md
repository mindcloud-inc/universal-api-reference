# E2B: Update Sandbox Network

Updates sandbox network settings in E2B.

```
PUT https://connect.mindcloud.co/v1/universal/e2B/latest/actions/update-sandbox-network
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/update-sandbox-network" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sandboxId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e2B/latest/actions/update-sandbox-network', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sandboxId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowOut[]` | array<string> | no | Allowed CIDR blocks, IP addresses, or domain names for sandbox egress traffic. |
| `denyOut[]` | array<string> | no | Denied CIDR blocks or IP addresses for sandbox egress traffic. |
| `sandboxId` | string | yes | Identifier of the sandbox. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native E2B API returns.

## Native endpoint

Through the native E2B API, this operation is `PUT /sandboxes/{sandboxID}/network` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sandbox-network.md) for the provider-specific parameters and requirements.

