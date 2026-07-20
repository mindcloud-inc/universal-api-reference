# MQTT: List Permissions By Role

Retrieves permissions for an MQTT role in HiveMQ Cloud.

```
GET https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-permissions-by-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MQTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-permissions-by-role?connectionId=$CONNECTION_ID&roleIdOrName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roleIdOrName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-permissions-by-role?${params}`, {
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
| `roleIdOrName` | string | yes | Role id or role name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "permissions": [
        {
          "permissionInfo": {
            "applyTo": "string",
            "description": "string",
            "id": "string",
            "name": "Ava Chen",
            "publishAllowed": true,
            "subscribeAllowed": true,
            "topic": "string"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `permissions[].permissionInfo.applyTo` | string |  |
| `permissions[].permissionInfo.description` | string |  |
| `permissions[].permissionInfo.id` | string |  |
| `permissions[].permissionInfo.name` | string |  |
| `permissions[].permissionInfo.publishAllowed` | boolean |  |
| `permissions[].permissionInfo.subscribeAllowed` | boolean |  |
| `permissions[].permissionInfo.topic` | string |  |

## Native endpoint

Through the native MQTT API, this operation is `GET /mqtt/roles/:roleIdOrName/permissions` (base URL `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-permissions-by-role.md) for the provider-specific parameters and requirements.

