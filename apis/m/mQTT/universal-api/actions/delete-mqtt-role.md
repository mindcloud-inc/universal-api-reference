# MQTT: Delete MQTT Role

Deletes an existing MQTT role from HiveMQ Cloud.

```
DELETE https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/delete-mqtt-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MQTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/delete-mqtt-role?connectionId=$CONNECTION_ID&roleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/delete-mqtt-role?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roleId` | number | yes | Numeric role identifier |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MQTT API returns.

## Native endpoint

Through the native MQTT API, this operation is `DELETE /mqtt/roles/:roleId` (base URL `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-mqtt-role.md) for the provider-specific parameters and requirements.

