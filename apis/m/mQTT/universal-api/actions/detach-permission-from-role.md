# MQTT: Detach Permission From Role

Updates an MQTT role in HiveMQ Cloud by detaching a permission.

```
PUT https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/detach-permission-from-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MQTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/detach-permission-from-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "permissionId": 1,
  "roleId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/detach-permission-from-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "permissionId": 1,
    "roleId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `permissionId` | number | yes | Numeric permission identifier |
| `roleId` | number | yes | Numeric role identifier |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MQTT API returns.

## Native endpoint

Through the native MQTT API, this operation is `PUT /mqtt/roles/:roleId/permissions/:permissionId/detach` (base URL `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detach-permission-from-role.md) for the provider-specific parameters and requirements.

